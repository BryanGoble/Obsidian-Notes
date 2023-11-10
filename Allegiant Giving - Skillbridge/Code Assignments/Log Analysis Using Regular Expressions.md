In this lab, we wrote an automation script that processed the system logs and generated two reports. One kept a count of all of the errors sorted by what the error was and how many times it occurred. The second kept track of user statistics to include the user and how many INFO and ERROR messages they had logged/tracked themselves.

```Python
#!/usr/bin/env python3
import re, csv, operator

error = {}
per_user = {}

pattern = r"(INFO|ERROR) ([\w' ]+|[\w\[\]#' ]+) (\(\w+\)|\(\w+\.\w+\))$"

with open('syslog.log', "r") as f:
  for line in f:
    result = re.search(pattern, line)
    if result is None:
      continue
    elif result.groups()[0] == "INFO":
      category = result.groups()[0]
      message = result.groups()[1]
      name = str(result.groups()[2])[1:-1]
      if name in per_user:
        user = per_user[name]
        user[category] += 1
      else:
        per_user[name] = {'INFO':1, 'ERROR':0}
    elif result.groups()[0] == "ERROR":
      category = result.groups()[0]
      message = result.groups()[1]
      name = str(result.groups()[2])[1:-1]
      error[message] = error.get(message, 0) + 1
      if name in per_user:
        user = per_user[name]
        user[category] += 1
      else:
        per_user[name] = {'INFO':0, 'ERROR':1}

sorted_logs = [("Error", "Count")] + sorted(error.items(), key = operator.itemgetter(1), reverse=True)

sorted_users = [("Username", "INFO", "ERROR")] + sorted(per_user.items())[0:8]

with open("error_message.csv", "w") as error_log:
  for line in sorted_logs:
    error_log.write("{}, {}\n".format(line[0], line[1]))

with open("user_statistics.csv", "w") as user_log:
  for line in sorted_users:
    if isinstance(line[1], dict):
      user_log.write("{}, {}, {}\n".format(line[0], line[1].get("INFO"), line[1].get("ERROR")))
    else:
      user_log.write("{}, {}, {}\n".format(line[0], line[1], line[2]))
```