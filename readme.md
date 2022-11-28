## Producing messages to OCI Streaming


*Example from documentation* 
https://docs.oracle.com/en-us/iaas/Content/Streaming/Tasks/streaming-quickstart-oci-sdk-for-go.htm
https://github.com/oracle/oci-go-sdk

## Quick shortcut to run on OCI Shell

```shell
mkdir producer
cd producer
go mod init example/producer
vi producer.go 
```
*paste* code from  See my   [producer.go](/producer.go/).   

You might need to run to update dependencies in mod :

```
go get -d github.com/oracle/oci-go-sdk/v49@latest
```

and 

```Go
const ociMessageEndpoint = "https://cell-1.streaming.eu-frankfurt-1.oci.oraclecloud.com"
const ociStreamOcid = "ocid1.stream.oc1.eu-frankfurt-1.amaaaaaauevftmqaikcwu43ouqq6lz2jhfrwevh3yrh2u6q4zpzcss5zvvuq"
const ociConfigFilePath = "/home/fernando_h/.oci/config"
const ociProfileName = "DEFAULT"
```

Where you should updater according to your configuration file.






