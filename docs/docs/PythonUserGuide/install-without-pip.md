## **Install without pip**
**Remark:**
- Only __Python 2.7__, __Python 3.5__ and __Python 3.6__ are supported for now.
- Note that __Python 3.6__ is only compatible with Spark 1.6.4, 2.0.3, 2.1.1 and 2.2.0. See [this issue](https://issues.apache.org/jira/browse/SPARK-19019) for more discussion.

1. [Download Spark](https://spark.apache.org/downloads.html)

2. You can download the BigDL release and nightly build from the [Release Page](../release-download.md)
  or build the BigDL package from [source](../ScalaUserGuide/install-build-src.md).

3. Install Python dependencies:
    * BigDL only depends on `Numpy` for now.
    * For Spark standalone cluster:
        * __If you're running in cluster mode, you need to install Python dependencies on both client and each worker node.__
        * Install Numpy: 
       ```sudo apt-get install python-numpy ``` (Ubuntu)
    * For Yarn cluster:
        - You can run BigDL Python programs on YARN clusters without changes to the cluster (e.g., no need to pre-install the Python dependencies). You  can first package all the required Python dependencies into a virtual environment on the localnode (where you will run the spark-submit command), and then directly use spark-submit to run the BigDL Python program on the YARN cluster (using that virtual environment). Please refer to this [Packing-dependencies](https://github.com/intel-analytics/BigDL/tree/master/pyspark/python_package) for more details.
   
