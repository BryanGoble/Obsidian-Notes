# Courses
1. [IBM Tools for Data Science (Week 1)](https://www.coursera.org/learn/open-source-tools-for-data-science/)
2. [IBM Tools for Data Science (Week 2)](https://www.coursera.org/learn/open-source-tools-for-data-science/)
3. [IBM Tools for Data Science (Week 3)](https://www.coursera.org/learn/open-source-tools-for-data-science/)
4. [IBM Tools for Data Science (Week 4)](https://www.coursera.org/learn/open-source-tools-for-data-science/)

## Overview - Data Science Tools

### Categories
- Data Management
	- Collecting, persisting, and retrieving data securely, efficiently and cost effectively
	- Data is collected from many sources
- Data Integration and Transformation
	- Extract, Transform, and Load (ETL)
	- Extract the data and save it in a central repository
	- Transforming the values, structure and format of the data
	- Transformed data is loaded back to a storage area
- Model Building
	- Train the data and analyze patterns using suitable machine learning algorithms
- Model Deployment
	- Integrating a model into a production environment
	- Uses APIs to enable data-based decisions
- Model Monitoring and Assessment
	- Tracks deployed models
	- Checks for accuracy, fairness, and robustness monitoring

### Requirements of Categories
- Execution Environments
	- Libraries for code compiling and system resources to execute and verify code
	- Cloud-based execution environments aren't tied to specific hardware or software
- Data Asset Management
	- Platform for organizing and managing the data
	- Replication, backup, and access right management
- Code Asset Management
	- Unified view where you manage an inventory of assets
	- Developers use versioning to track and manage changes to a software project's code
	- Collaboration allows diverse people to share and update the same project together
- Development Environments
	- Integrated development environments (IDEs) provide a workspace and tolls to work on source code.
	- IDEs like IBM Watson Studio provide testing and simulation tools to emulate the real world so you can see how your code will behave after it is deployed.

### Open Source Data Management Tools
- MongoDB
- CouchDB
- Cassandra
- Hadoop File System
- Ceph
- ElasticSearch
- MySQL
- PostgreSQL

### Data Integration and Transformation
- Is used for ETL or ELT
- Commonly referred to as Data Refinery and Cleansing
- Using:
	- Kubeflow
	- Apache Kafka
	- Apache Nifi
	- Spark SQL
	- Node-Red
	- Apache Airflow

### Data Visualization
- Open Source Tools:
	- HUE
	- Kibana
	- Superset
	- PixieDust

### Model Deployment
- Can be deployed to:
	- PredictionIO
	- Seldon
	- Kubernetes
	- Red Hat OpenShift
	- mleap
	- TensorFlow Serving
	- TensorFlow Lite

### Model Monitoring and Assessment
- Tools to keep track of machine learning model's prediction performance to maintain outdated models
	- ModelDB
	- Prometheus
	- Adversarial Robustness 360 Toolbox
	- AI Explainability 360
	- AI Fairness 360 Open Source Toolkit

### Code Asset Management
- Tools for code asset management, also known as version management or version control:
	- Git
	- GitHub
	- GitLab
	- BitBucket

### Data Asset Management
- Tools for data asset management, also known as data governance or data lineage:
	- Apache Atlas
	- Egeria
	- Kylo

## Week 2 Summary

- You should select a language to learn depending on your needs, the problems you are trying to solve, and whom you are solving them for.
- The popular languages are Python, R, SQL, Scala, Java, C++, and Julia.
- For data science, you can use Python's scientific computing libraries like Pandas, NumPy, SciPy, and Matplotlib.
- Python can also be used for Natural Language Processing (NLP) using the Natural Language Toolkit (NLTK).
- Python is open source, and R is free software.
- R language’s array-oriented syntax makes it easier to translate from math to code for learners with no or minimal programming background.
- SQL is different from other software development languages because it is a non-procedural language.
- SQL was designed for managing data in relational databases.
- If you learn SQL and use it with one database, you can apply your SQL knowledge with many other databases easily.
- Data science tools built with Java include Weka, Java-ML, Apache MLlib, and Deeplearning4.
- For data science, popular program built with Scala is Apache Spark which includes Shark, MLlib, GraphX, and Spark Streaming.
- Programs built for Data Science with JavaScript include TensorFlow.js and R-js.
- One great application of Julia for Data Science is JuliaDB.

## Week 3 Summary

- Libraries usually contain built-in modules that provide different functionalities.
- You can use data visualization methods to communicate with others and display meaningful results of an analysis. 
- For machine learning, the Scikit-learn library contains tools for statistical modeling, including regression, classification, clustering, and so on.
- Large-scale production of deep-learning models use TensorFlow, a low-level framework. 
	- The Julia API can be used with TensorFlow
- Apache Spark is a general-purpose cluster-computing framework that allows you to process data using compute clusters.
- An application programming interface (API) allows communication between two pieces of software.
- API is the part of the library you see while the library contains all the components of the program. 
- Representational State Transfer (REST) APIs allow you to communicate through the internet and take advantage of resources like storage, data, artificially intelligent algorithms, and much more.
- Open data is fundamental to Data Science.
- Community Data License Agreement makes it easier to share open data.
- The IBM Data Asset eXchange (DAX) site contains high-quality open data sets.
- DAX open data sets include tutorial notebooks that provide basic and advanced walk-throughs for developers.
- DAX notebooks open in Watson Studio.
- Machine learning (ML) uses algorithms – also known as “models” – to identify patterns in the data. 
- Types of ML are Supervised, Unsupervised, and Reinforcement.
	- Supervised learning comprises two types of models, regression and classification.
		- Supervised is used to solve regression and classification problems
- Deep learning refers to a general set of models and techniques that loosely emulate the way the human brain solves a wide range of problems.
	- PyTorch is a deep learning library in Python used for experimentation
- The Model Asset eXchange is a free, open-source repository for ready-to-use and customizable deep-learning microservices.
- MAX model-serving microservices are built and distributed on GitHub as open-source Docker images.
- You can use Red Hat OpenShift, a Kubernetes platform, to automate deployment, scaling, and management of microservices.
- Ml-exchange.org has multiple predefined models.
- According to the license, CDLA-Sharing, it stipulates that the modified version of the open data should be published under the same license terms.

## Week 4 Summary

- Jupyter Notebooks are used in Data Science for recording experiments and projects.
- Jupyter Lab is compatible with many files and Data Science languages. 
- There are different ways to install and use Jupyter Notebooks.
- How to run, delete, and insert a code cell in Jupyter Notebooks.
- How to run multiple notebooks at the same time.
- How to present a notebook using a combination of Markdown and code cells.
- How to shut down your notebook sessions after you have completed your work on them.
- Jupyter implements a two-process model with a kernel and a client.
- The notebook server is responsible for saving and loading the notebooks.
- The kernel executes the cells of code contained in the Notebook. 
- The Jupyter architecture uses the NB convert tool to convert files to other formats.
- Jupyter implements a two-process model with a kernel and a client.
- The Notebook server is responsible for saving and loading the notebooks.
- The Jupyter architecture uses the NB convert tool to convert files to other formats.
- The Anaconda Navigator GUI can launch multiple applications on a local device.
- Jupyter environments in the Anaconda Navigator include JupyterLab and VS Code.
- You can download Jupyter environments separately from the Anaconda Navigator, but they may not be configured properly.
- The Anaconda Navigator GUI can launch multiple applications.
- Additional open-source Jupyter environments include JupyterLab, JupyterLite, VS Code, and Google Colaboratory. 
- JupyterLite is a browser-based tool.

## Week 5 Summary

- The capabilities of R and its uses in Data Science.  
- The RStudio interface for running R codes. 
- Popular R packages for Data Science.
- Popular data visualization packages in R.
- Plotting with the inbuilt R plot function.
- Plotting with ggplot.
- Machine Learning is used with Caret
- Adding titles and changing the axis names using the ggtitle and lab’s function.
- A Distributed Version Control System (DVCS) keeps track of changes to code, regardless of where it is stored.
- Version control allows multiple users to work on the same codebase or repository, mirroring the codebase on their own computers if needed, while the distributed version control software helps manage synchronization amongst the various codebase mirrors.
- Repositories are storage structures that:
    - Store the code
    - Track issues and changes
    - Enable you to collaborate with others
- Git is one of the most popular distributed version control systems. 
- GitHub, GitLab and Bitbucket are examples of hosted version control systems.
- Branches are used to isolate changes to code. When the changes are complete, they can be merged back into the main branch.
- Repositories can be cloned to make it possible to work locally, then sync changes back to the original.

## Week 7 Summary

- Watson Studio is a helpful tool for:
    - Analyzing and viewing data
    - Cleaning and shaping data
    - Embedding data into streams
    - Creating, training, and deploying
- Learning Watson Studio promotes career growth.
- Learning Watson Studio is easy and requires no special skills.
- Watson Studio offers many available resources.
- You must create an IBM Cloud account to use Watson Studio.
- You can open Watson Studio by clicking Catalog on the IBM Cloud dashboard and then AI/Machine Learning.
- You can create an empty project or a project from a sample or file by selecting the Work with data option.
- You can add a storage service by clicking Add and then selecting the storage service of your choice.
- You can add or create a new notebook by clicking **New asset** on the project home page under the **Assets** tab.
- You can share your notebook without sharing the sensitive cells.
- Jobs are created and scheduled from the **Create a job** icon in the notebook action bar.
- Jobs can be viewed, edited, or deleted on the project home page under the **Jobs** tab.
- Jupyter Notebook runtime environments and templates can be found on the Environments tab in the Home Page.
- You can create and change new Jupyter Notebook templates.
- Watson Studio accounts can be integrated into GitHub.
- You can push notebooks from Watson Studio to GitHub.

