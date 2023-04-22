# booking-etl
1. Install Java
2. Download and Install Anaconda for Jupyet notebook to run python code.
 https://www.anaconda.com/download

3. Click the below link to Download Spark to download the spark-3.1.1-bin-hadoop2.7.tgz.
    https://www.apache.org/dyn/closer.lua/spark/spark-3.2.4/spark-3.2.4-bin-hadoop2.7.tgz
5. In order to install Apache Spark, there is no need to run any installer. You can extract the files from the downloaded zip file using winzip
6. Unzip the file in this location C:\Users\<your_user_name>\Desktop\spark\spark-3.1.1-bin-hadoop2.7 and rename spark-3.1.1-bin-hadoop2.7 as "SPARK_HOME".
7. Download the winutils.exe for the version of hadoop against which your Spark installation.
   https://github.com/steveloughran/winutils
   
7. Create hadoop/bin directory inside C:\Users\<your_user_name>\Desktop\spark\SPARK_HOME.
8. Create a system environment variable in windows.
   
   Define User variable path:
     SPARK_HOME: C:\Users\<your_user_name>\Desktop\spark\SPARK_HOME
     HADOOP_HOME: C:\Users\<your_user_name>\Desktop\spark\SPARK_HOME\hadoop
   
   Define System Variable:
     SPARK_HOME: C:\Users\<your_user_name>\Desktop\spark\SPARK_HOME
     HADOOP_HOME: %SPARK_HOME%\hadoop
     
9. Test Spark From Jupyter Notebook.
   import findspark
   findspark.init()

#### Initialize spark sesssion
import pyspark
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("bookings-etl").getOrCreate()
   
   
