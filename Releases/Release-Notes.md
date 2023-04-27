# Azure HDInsight release notes

This article provides information about the most recent Azure HDInsight release updates.

## Summary
Azure HDInsight is one of the most popular services among enterprise customers for open-source analytics on Azure.
[Subscribe to our release notes](./subscribe-to-hdi-release-notes-repo.md) and watch releases on [this GitHub repository](https://github.com/hdinsight/release-notes/releases).

## Release date: February 28, 2023

This release applies to HDInsight 4.0. 5.0, and 5.1. HDInsight release will be available to all regions over several days. This release is applicable for image number *2302250400*. [How to check the image number?](https://learn.microsoft.com/azure/hdinsight/view-hindsight-cluster-image-version)

HDInsight uses safe deployment practices, which involve gradual region deployment. it may take up to 10 business days for a new release or a new version to be available in all regions.

**OS versions**

* HDInsight 4.0: Ubuntu 18.04.5 LTS Linux Kernel 5.4
* HDInsight 5.0: Ubuntu 18.04.5 LTS Linux Kernel 5.4

For workload specific versions, see

[HDInsight 4.x component versions](https://learn.microsoft.com/azure/hdinsight/hdinsight-40-component-versioning)
[HDInsight 5.x component versions](https://learn.microsoft.com/azure/hdinsight/hdinsight-5x-component-versioning#open-source-components-available-with-hdinsight-version-5x)

**Note:**
Microsoft has issued [CVE-2023-23408](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-23408), which is fixed on the current release and customers are advised to upgrade their clusters to latest image.

### What's new?

**HDInsight 5.1**

We have started rolling out a new version of HDInsight 5.1. All new open-source releases added as incremental releases on HDInsight 5.1.

For more information, see [HDInsight 5.x version](https://learn.microsoft.com/azure/hdinsight/hdinsight-5x-component-versioning)

**Kafka 3.2.0 Upgrade (Preview)** 

* Kafka 3.2.0 includes several significant new features/improvements.
	* Upgraded Zookeeper to 3.6.3
	* Kafka Streams support
	* Stronger delivery guarantees for the Kafka producer enabled by default.
	* log4j 1.x replaced with reload4j.
	* Send a hint to the partition leader to recover the partition.
	* `JoinGroupRequest` and `LeaveGroupRequest` have a reason attached.
	* Added Broker count metrics8. 
	* Mirror Maker2 improvements.

**HBase 2.4.11 Upgrade (Preview)**
* This version has new features such as the addition of new caching mechanism types for block cache, the ability to alter `hbase:meta table` and view the `hbase:meta` table from the HBase WEB UI. 

**Phoenix 5.1.2 Upgrade (Preview)**
 * Phoenix version upgraded to 5.1.2 in this release. This upgrade includes the Phoenix Query Server. The Phoenix Query Server proxies the standard Phoenix JDBC driver and provides a backwards-compatible wire protocol to invoke that JDBC driver.
 
**Ambari CVEs**
  * Multiple Ambari CVEs are fixed.
 
**Note:**
ESP isn't supported for Kafka and HBase in this release.

### End of support

End of support for Azure HDInsight clusters on Spark 2.4 February 10, 2024. For more information, see [Spark versions supported in Azure HDInsight](https://learn.microsoft.com/azure/hdinsight/hdinsight-40-component-versioning#spark-versions-supported-in-azure-hdinsight)

### Coming soon
* Autoscale
  * Autoscale with improved latency and several improvements
* Cluster name change limitation 
  * The max length of cluster name will be changed to 45 from 59 in Public, Mooncake and Fairfax. 
* Cluster permissions for secure storage  
  * Customers can specify (during cluster creation) whether a secure channel should be used for HDInsight cluster nodes to contact the storage account. 
* Non-ESP ABFS clusters [Cluster Permissions for World Readable] 
  * Plan to introduce a change in non-ESP ABFS clusters, which restricts non-Hadoop group users from executing Hadoop commands for storage operations. This change to improve cluster security posture. Customers need to plan for the updates.
* Open-source upgrades
  * Apache Spark 3.3.0 and Hadoop 3.3.4 are under development on HDInsight 5.1 and will include several significant new features, performance and other improvements.

 **NOTE:**
 We advise customers to use to latest versions of HDInsight [Images](https://learn.microsoft.com/en-us/azure/hdinsight/view-hindsight-cluster-image-version) as they bring in the best of open-source updates,  Azure updates and security fixes.
