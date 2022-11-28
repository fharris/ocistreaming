## Producing messages to OCI Streaming


# Example from documentation: 
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

You might need to run :

```
go get -d github.com/oracle/oci-go-sdk/v49@latest
```





