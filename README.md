# datastore

The goal is to create a reusable read-optimised microservice for protocol buffer data storage.

## Architecture

The data will be stored on a hierarchy of datastores made up of:

- Memcached cluster
- DynamoDB
- S3

Writes will go into DynamoDB and DynamoDB Stream will be used to keep Memcached and S3 synchronised.

In order to make this microservice reusable, gRPC will be used.
