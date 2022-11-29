# Producing messages to OCI Streaming with Go


*Example from documentation* 
https://docs.oracle.com/en-us/iaas/Content/Streaming/Tasks/streaming-quickstart-oci-sdk-for-go.htm
https://github.com/oracle/oci-go-sdk

## Quick shortcut to run on OCI Shell

Open your OCI Shell:


```shell
mkdir producer
cd producer
go mod init example/producer
vi producer.go 
```
*paste* code from  [producer.go](/producer.go/).   

You might need  to update dependencies in mod with below command:

```
go get -d github.com/oracle/oci-go-sdk/v49@latest
```

and 

```Go
const ociMessageEndpoint = "https://cell-1.streaming.eu-frankfurt-1.oci.oraclecloud.com"
const ociStreamOcid = "ocid1.stream.oc1.eu-frankfurt-1.amaaaaa..."
const ociConfigFilePath = "/home/fernando_h/.oci/config"
const ociProfileName = "DEFAULT"
```


Where you should update according to your OCI configuration file and OCI Streaming Service streamOCID and Endpoint.

# Consuming messages from OCI Streaming with Java

*Example from documentation* 
https://docs.oracle.com/en-us/iaas/Content/Streaming/Tasks/streaming-quickstart-oci-sdk-for-java.htm#java-sdk-streaming-quickstart
https://github.com/oracle/oci-java-sdk


## Quick shortcut to run on OCI Shell

Open your OCI Shell:

```shell
mkdir consumer
cd consumer
mvn -B archetype:generate -DgroupId=com.oci.stream -DartifactId=Consumer -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4
vi Consumer/pom.xml
```

Add dependencies to pom:
```xml
<dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.11</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
```

mvn install exec:java -Dexec.mainClass=com.oci.stream.App
```

Create a new file with 
