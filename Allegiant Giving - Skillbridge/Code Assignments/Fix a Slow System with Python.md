We were instructed to write a python script that either synced or copied data from different multimedia projects from the source location to the destination using `rsync` command. This reduced the backup time by taking advantage of the idle CPU cores for parallel processing using multiprocessing.

```Python
#!/usr/bin/env python3
import subprocess, os
from multiprocessing import Pool

def backup(src):
  dest = os.getcwd() + "/data/prod_backup/"
  print(f"Backing up {src} into {dest}")
  subprocess.call(["rsync", "-arq", src, dest])

if __name__ == "__main__":
  src = os.getcwd() + "/data/prod/"
  list_of_files = os.listdir(src)
  all_files = []

  for value in list_of_files:
    full_path = os.path.join(src, value)
    all_files.append(full_path)

  with Pool(len(all_files)) as pool:
    pool.map(backup, all_files)
```