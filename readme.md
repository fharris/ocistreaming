# Producing messages to OCI Streaming


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






