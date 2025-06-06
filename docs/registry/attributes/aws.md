<!-- NOTE: THIS FILE IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/attribute_namespace.md.j2 -->

# AWS

- [General AWS Attributes](#general-aws-attributes)
- [Amazon Bedrock Attributes](#amazon-bedrock-attributes)
- [Amazon DynamoDB Attributes](#amazon-dynamodb-attributes)
- [Amazon ECS Attributes](#amazon-ecs-attributes)
- [Amazon EKS Attributes](#amazon-eks-attributes)
- [Amazon Kinesis Attributes](#amazon-kinesis-attributes)
- [Amazon Lambda Attributes](#amazon-lambda-attributes)
- [Amazon Logs Attributes](#amazon-logs-attributes)
- [Amazon S3 Attributes](#amazon-s3-attributes)
- [Amazon Secrets Manager Attributes](#amazon-secrets-manager-attributes)
- [Amazon SNS Attributes](#amazon-sns-attributes)
- [Amazon SQS Attributes](#amazon-sqs-attributes)
- [Amazon Step Functions Attributes](#amazon-step-functions-attributes)

## General AWS Attributes

This section defines generic attributes for AWS services.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-extended-request-id" href="#aws-extended-request-id">`aws.extended_request_id`</a> | string | The AWS extended request ID as returned in the response header `x-amz-id-2`. | `wzHcyEWfmOGDIE5QOhTAqFDoDWP3y8IUvpNINCwL9N4TEHbUw0/gZJ+VZTmCNCWR7fezEN3eCiQ=` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-request-id" href="#aws-request-id">`aws.request_id`</a> | string | The AWS request ID as returned in the response headers `x-amzn-requestid`, `x-amzn-request-id` or `x-amz-request-id`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon Bedrock Attributes

This document defines attributes for AWS Bedrock.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-bedrock-guardrail-id" href="#aws-bedrock-guardrail-id">`aws.bedrock.guardrail.id`</a> | string | The unique identifier of the AWS Bedrock Guardrail. A [guardrail](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html) helps safeguard and prevent unwanted behavior from model responses or user messages. | `sgi5gkybzqak` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-bedrock-knowledge-base-id" href="#aws-bedrock-knowledge-base-id">`aws.bedrock.knowledge_base.id`</a> | string | The unique identifier of the AWS Bedrock Knowledge base. A [knowledge base](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html) is a bank of information that can be queried by models to generate more relevant responses and augment prompts. | `XFWUPB9PAW` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon DynamoDB Attributes

This document defines attributes for AWS DynamoDB.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-dynamodb-attribute-definitions" href="#aws-dynamodb-attribute-definitions">`aws.dynamodb.attribute_definitions`</a> | string[] | The JSON-serialized value of each item in the `AttributeDefinitions` request field. | `["{ \"AttributeName\": \"string\", \"AttributeType\": \"string\" }"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-attributes-to-get" href="#aws-dynamodb-attributes-to-get">`aws.dynamodb.attributes_to_get`</a> | string[] | The value of the `AttributesToGet` request parameter. | `["lives", "id"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-consistent-read" href="#aws-dynamodb-consistent-read">`aws.dynamodb.consistent_read`</a> | boolean | The value of the `ConsistentRead` request parameter. |  | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-consumed-capacity" href="#aws-dynamodb-consumed-capacity">`aws.dynamodb.consumed_capacity`</a> | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `["{ \"CapacityUnits\": number, \"GlobalSecondaryIndexes\": { \"string\" : { \"CapacityUnits\": number, \"ReadCapacityUnits\": number, \"WriteCapacityUnits\": number } }, \"LocalSecondaryIndexes\": { \"string\" : { \"CapacityUnits\": number, \"ReadCapacityUnits\": number, \"WriteCapacityUnits\": number } }, \"ReadCapacityUnits\": number, \"Table\": { \"CapacityUnits\": number, \"ReadCapacityUnits\": number, \"WriteCapacityUnits\": number }, \"TableName\": \"string\", \"WriteCapacityUnits\": number }"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-count" href="#aws-dynamodb-count">`aws.dynamodb.count`</a> | int | The value of the `Count` response parameter. | `10` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-exclusive-start-table" href="#aws-dynamodb-exclusive-start-table">`aws.dynamodb.exclusive_start_table`</a> | string | The value of the `ExclusiveStartTableName` request parameter. | `Users`; `CatsTable` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-global-secondary-index-updates" href="#aws-dynamodb-global-secondary-index-updates">`aws.dynamodb.global_secondary_index_updates`</a> | string[] | The JSON-serialized value of each item in the `GlobalSecondaryIndexUpdates` request field. | `["{ \"Create\": { \"IndexName\": \"string\", \"KeySchema\": [ { \"AttributeName\": \"string\", \"KeyType\": \"string\" } ], \"Projection\": { \"NonKeyAttributes\": [ \"string\" ], \"ProjectionType\": \"string\" }, \"ProvisionedThroughput\": { \"ReadCapacityUnits\": number, \"WriteCapacityUnits\": number } }"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-global-secondary-indexes" href="#aws-dynamodb-global-secondary-indexes">`aws.dynamodb.global_secondary_indexes`</a> | string[] | The JSON-serialized value of each item of the `GlobalSecondaryIndexes` request field | `["{ \"IndexName\": \"string\", \"KeySchema\": [ { \"AttributeName\": \"string\", \"KeyType\": \"string\" } ], \"Projection\": { \"NonKeyAttributes\": [ \"string\" ], \"ProjectionType\": \"string\" }, \"ProvisionedThroughput\": { \"ReadCapacityUnits\": number, \"WriteCapacityUnits\": number } }"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-index-name" href="#aws-dynamodb-index-name">`aws.dynamodb.index_name`</a> | string | The value of the `IndexName` request parameter. | `name_to_group` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-item-collection-metrics" href="#aws-dynamodb-item-collection-metrics">`aws.dynamodb.item_collection_metrics`</a> | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-limit" href="#aws-dynamodb-limit">`aws.dynamodb.limit`</a> | int | The value of the `Limit` request parameter. | `10` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-local-secondary-indexes" href="#aws-dynamodb-local-secondary-indexes">`aws.dynamodb.local_secondary_indexes`</a> | string[] | The JSON-serialized value of each item of the `LocalSecondaryIndexes` request field. | `["{ \"IndexArn\": \"string\", \"IndexName\": \"string\", \"IndexSizeBytes\": number, \"ItemCount\": number, \"KeySchema\": [ { \"AttributeName\": \"string\", \"KeyType\": \"string\" } ], \"Projection\": { \"NonKeyAttributes\": [ \"string\" ], \"ProjectionType\": \"string\" } }"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-projection" href="#aws-dynamodb-projection">`aws.dynamodb.projection`</a> | string | The value of the `ProjectionExpression` request parameter. | `Title`; `Title, Price, Color`; `Title, Description, RelatedItems, ProductReviews` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-provisioned-read-capacity" href="#aws-dynamodb-provisioned-read-capacity">`aws.dynamodb.provisioned_read_capacity`</a> | double | The value of the `ProvisionedThroughput.ReadCapacityUnits` request parameter. | `1.0`; `2.0` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-provisioned-write-capacity" href="#aws-dynamodb-provisioned-write-capacity">`aws.dynamodb.provisioned_write_capacity`</a> | double | The value of the `ProvisionedThroughput.WriteCapacityUnits` request parameter. | `1.0`; `2.0` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-scan-forward" href="#aws-dynamodb-scan-forward">`aws.dynamodb.scan_forward`</a> | boolean | The value of the `ScanIndexForward` request parameter. |  | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-scanned-count" href="#aws-dynamodb-scanned-count">`aws.dynamodb.scanned_count`</a> | int | The value of the `ScannedCount` response parameter. | `50` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-segment" href="#aws-dynamodb-segment">`aws.dynamodb.segment`</a> | int | The value of the `Segment` request parameter. | `10` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-select" href="#aws-dynamodb-select">`aws.dynamodb.select`</a> | string | The value of the `Select` request parameter. | `ALL_ATTRIBUTES`; `COUNT` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-table-count" href="#aws-dynamodb-table-count">`aws.dynamodb.table_count`</a> | int | The number of items in the `TableNames` response parameter. | `20` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-table-names" href="#aws-dynamodb-table-names">`aws.dynamodb.table_names`</a> | string[] | The keys in the `RequestItems` object field. | `["Users", "Cats"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-dynamodb-total-segments" href="#aws-dynamodb-total-segments">`aws.dynamodb.total_segments`</a> | int | The value of the `TotalSegments` request parameter. | `100` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon ECS Attributes

This document defines attributes for AWS Elastic Container Service (ECS).

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-ecs-cluster-arn" href="#aws-ecs-cluster-arn">`aws.ecs.cluster.arn`</a> | string | The ARN of an [ECS cluster](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/clusters.html). | `arn:aws:ecs:us-west-2:123456789123:cluster/my-cluster` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-container-arn" href="#aws-ecs-container-arn">`aws.ecs.container.arn`</a> | string | The Amazon Resource Name (ARN) of an [ECS container instance](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ECS_instances.html). | `arn:aws:ecs:us-west-1:123456789123:container/32624152-9086-4f0e-acae-1a75b14fe4d9` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-launchtype" href="#aws-ecs-launchtype">`aws.ecs.launchtype`</a> | string | The [launch type](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_types.html) for an ECS task. | `ec2`; `fargate` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-task-arn" href="#aws-ecs-task-arn">`aws.ecs.task.arn`</a> | string | The ARN of a running [ECS task](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-account-settings.html#ecs-resource-ids). | `arn:aws:ecs:us-west-1:123456789123:task/10838bed-421f-43ef-870a-f43feacbbb5b`; `arn:aws:ecs:us-west-1:123456789123:task/my-cluster/task-id/23ebb8ac-c18f-46c6-8bbe-d55d0e37cfbd` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-task-family" href="#aws-ecs-task-family">`aws.ecs.task.family`</a> | string | The family name of the [ECS task definition](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definitions.html) used to create the ECS task. | `opentelemetry-family` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-task-id" href="#aws-ecs-task-id">`aws.ecs.task.id`</a> | string | The ID of a running ECS task. The ID MUST be extracted from `task.arn`. | `10838bed-421f-43ef-870a-f43feacbbb5b`; `23ebb8ac-c18f-46c6-8bbe-d55d0e37cfbd` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-ecs-task-revision" href="#aws-ecs-task-revision">`aws.ecs.task.revision`</a> | string | The revision for the task definition used to create the ECS task. | `8`; `26` | ![Development](https://img.shields.io/badge/-development-blue) |

---

`aws.ecs.launchtype` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `ec2` | ec2 | ![Development](https://img.shields.io/badge/-development-blue) |
| `fargate` | fargate | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon EKS Attributes

This document defines attributes for AWS Elastic Kubernetes Service (EKS).

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-eks-cluster-arn" href="#aws-eks-cluster-arn">`aws.eks.cluster.arn`</a> | string | The ARN of an EKS cluster. | `arn:aws:ecs:us-west-2:123456789123:cluster/my-cluster` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon Kinesis Attributes

This document defines attributes for AWS Kinesis.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-kinesis-stream-name" href="#aws-kinesis-stream-name">`aws.kinesis.stream_name`</a> | string | The name of the AWS Kinesis [stream](https://docs.aws.amazon.com/streams/latest/dev/introduction.html) the request refers to. Corresponds to the `--stream-name` parameter of the Kinesis [describe-stream](https://docs.aws.amazon.com/cli/latest/reference/kinesis/describe-stream.html) operation. | `some-stream-name` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon Lambda Attributes

This document defines attributes for AWS Lambda.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-lambda-invoked-arn" href="#aws-lambda-invoked-arn">`aws.lambda.invoked_arn`</a> | string | The full invoked ARN as provided on the `Context` passed to the function (`Lambda-Runtime-Invoked-Function-Arn` header on the `/runtime/invocation/next` applicable). [1] | `arn:aws:lambda:us-east-1:123456:function:myfunction:myalias` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-lambda-resource-mapping-id" href="#aws-lambda-resource-mapping-id">`aws.lambda.resource_mapping.id`</a> | string | The UUID of the [AWS Lambda EvenSource Mapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html). An event source is mapped to a lambda function. It's contents are read by Lambda and used to trigger a function. This isn't available in the lambda execution context or the lambda runtime environtment. This is going to be populated by the AWS SDK for each language when that UUID is present. Some of these operations are Create/Delete/Get/List/Update EventSourceMapping. | `587ad24b-03b9-4413-8202-bbd56b36e5b7` | ![Development](https://img.shields.io/badge/-development-blue) |

**[1] `aws.lambda.invoked_arn`:** This may be different from `cloud.resource_id` if an alias is involved.

## Amazon Logs Attributes

This document defines attributes for AWS Logs.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-log-group-arns" href="#aws-log-group-arns">`aws.log.group.arns`</a> | string[] | The Amazon Resource Name(s) (ARN) of the AWS log group(s). [2] | `["arn:aws:logs:us-west-1:123456789012:log-group:/aws/my/group:*"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-log-group-names" href="#aws-log-group-names">`aws.log.group.names`</a> | string[] | The name(s) of the AWS log group(s) an application is writing to. [3] | `["/aws/lambda/my-function", "opentelemetry-service"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-log-stream-arns" href="#aws-log-stream-arns">`aws.log.stream.arns`</a> | string[] | The ARN(s) of the AWS log stream(s). [4] | `["arn:aws:logs:us-west-1:123456789012:log-group:/aws/my/group:log-stream:logs/main/10838bed-421f-43ef-870a-f43feacbbb5b"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-log-stream-names" href="#aws-log-stream-names">`aws.log.stream.names`</a> | string[] | The name(s) of the AWS log stream(s) an application is writing to. | `["logs/main/10838bed-421f-43ef-870a-f43feacbbb5b"]` | ![Development](https://img.shields.io/badge/-development-blue) |

**[2] `aws.log.group.arns`:** See the [log group ARN format documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/iam-access-control-overview-cwl.html#CWL_ARN_Format).

**[3] `aws.log.group.names`:** Multiple log groups must be supported for cases like multi-container applications, where a single application has sidecar containers, and each write to their own log group.

**[4] `aws.log.stream.arns`:** See the [log stream ARN format documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/iam-access-control-overview-cwl.html#CWL_ARN_Format). One log group can contain several log streams, so these ARNs necessarily identify both a log group and a log stream.

## Amazon S3 Attributes

This document defines attributes for AWS S3.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-s3-bucket" href="#aws-s3-bucket">`aws.s3.bucket`</a> | string | The S3 bucket name the request refers to. Corresponds to the `--bucket` parameter of the [S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/index.html) operations. [5] | `some-bucket-name` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-s3-copy-source" href="#aws-s3-copy-source">`aws.s3.copy_source`</a> | string | The source object (in the form `bucket`/`key`) for the copy operation. [6] | `someFile.yml` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-s3-delete" href="#aws-s3-delete">`aws.s3.delete`</a> | string | The delete request container that specifies the objects to be deleted. [7] | `Objects=[{Key=string,VersionId=string},{Key=string,VersionId=string}],Quiet=boolean` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-s3-key" href="#aws-s3-key">`aws.s3.key`</a> | string | The S3 object key the request refers to. Corresponds to the `--key` parameter of the [S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/index.html) operations. [8] | `someFile.yml` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-s3-part-number" href="#aws-s3-part-number">`aws.s3.part_number`</a> | int | The part number of the part being uploaded in a multipart-upload operation. This is a positive integer between 1 and 10,000. [9] | `3456` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-s3-upload-id" href="#aws-s3-upload-id">`aws.s3.upload_id`</a> | string | Upload ID that identifies the multipart upload. [10] | `dfRtDYWFbkRONycy.Yxwh66Yjlx.cph0gtNBtJ` | ![Development](https://img.shields.io/badge/-development-blue) |

**[5] `aws.s3.bucket`:** The `bucket` attribute is applicable to all S3 operations that reference a bucket, i.e. that require the bucket name as a mandatory parameter.
This applies to almost all S3 operations except `list-buckets`.

**[6] `aws.s3.copy_source`:** The `copy_source` attribute applies to S3 copy operations and corresponds to the `--copy-source` parameter
of the [copy-object operation within the S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/copy-object.html).
This applies in particular to the following operations:

- [copy-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/copy-object.html)
- [upload-part-copy](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part-copy.html)

**[7] `aws.s3.delete`:** The `delete` attribute is only applicable to the [delete-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/delete-object.html) operation.
The `delete` attribute corresponds to the `--delete` parameter of the
[delete-objects operation within the S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/delete-objects.html).

**[8] `aws.s3.key`:** The `key` attribute is applicable to all object-related S3 operations, i.e. that require the object key as a mandatory parameter.
This applies in particular to the following operations:

- [copy-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/copy-object.html)
- [delete-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/delete-object.html)
- [get-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/get-object.html)
- [head-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/head-object.html)
- [put-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/put-object.html)
- [restore-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/restore-object.html)
- [select-object-content](https://docs.aws.amazon.com/cli/latest/reference/s3api/select-object-content.html)
- [abort-multipart-upload](https://docs.aws.amazon.com/cli/latest/reference/s3api/abort-multipart-upload.html)
- [complete-multipart-upload](https://docs.aws.amazon.com/cli/latest/reference/s3api/complete-multipart-upload.html)
- [create-multipart-upload](https://docs.aws.amazon.com/cli/latest/reference/s3api/create-multipart-upload.html)
- [list-parts](https://docs.aws.amazon.com/cli/latest/reference/s3api/list-parts.html)
- [upload-part](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part.html)
- [upload-part-copy](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part-copy.html)

**[9] `aws.s3.part_number`:** The `part_number` attribute is only applicable to the [upload-part](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part.html)
and [upload-part-copy](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part-copy.html) operations.
The `part_number` attribute corresponds to the `--part-number` parameter of the
[upload-part operation within the S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part.html).

**[10] `aws.s3.upload_id`:** The `upload_id` attribute applies to S3 multipart-upload operations and corresponds to the `--upload-id` parameter
of the [S3 API](https://docs.aws.amazon.com/cli/latest/reference/s3api/index.html) multipart operations.
This applies in particular to the following operations:

- [abort-multipart-upload](https://docs.aws.amazon.com/cli/latest/reference/s3api/abort-multipart-upload.html)
- [complete-multipart-upload](https://docs.aws.amazon.com/cli/latest/reference/s3api/complete-multipart-upload.html)
- [list-parts](https://docs.aws.amazon.com/cli/latest/reference/s3api/list-parts.html)
- [upload-part](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part.html)
- [upload-part-copy](https://docs.aws.amazon.com/cli/latest/reference/s3api/upload-part-copy.html)

## Amazon Secrets Manager Attributes

This document defines attributes for AWS Secrets Manager.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-secretsmanager-secret-arn" href="#aws-secretsmanager-secret-arn">`aws.secretsmanager.secret.arn`</a> | string | The ARN of the Secret stored in the Secrets Mangger | `arn:aws:secretsmanager:us-east-1:123456789012:secret:SecretName-6RandomCharacters` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon SNS Attributes

This document defines attributes for AWS SNS.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-sns-topic-arn" href="#aws-sns-topic-arn">`aws.sns.topic.arn`</a> | string | The ARN of the AWS SNS Topic. An Amazon SNS [topic](https://docs.aws.amazon.com/sns/latest/dg/sns-create-topic.html) is a logical access point that acts as a communication channel. | `arn:aws:sns:us-east-1:123456789012:mystack-mytopic-NZJ5JSMVGFIE` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon SQS Attributes

This document defines attributes for AWS SQS.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-sqs-queue-url" href="#aws-sqs-queue-url">`aws.sqs.queue.url`</a> | string | The URL of the AWS SQS Queue. It's a unique identifier for a queue in Amazon Simple Queue Service (SQS) and is used to access the queue and perform actions on it. | `https://sqs.us-east-1.amazonaws.com/123456789012/MyQueue` | ![Development](https://img.shields.io/badge/-development-blue) |

## Amazon Step Functions Attributes

This document defines attributes for AWS Step Functions.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="aws-step-functions-activity-arn" href="#aws-step-functions-activity-arn">`aws.step_functions.activity.arn`</a> | string | The ARN of the AWS Step Functions Activity. | `arn:aws:states:us-east-1:123456789012:activity:get-greeting` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="aws-step-functions-state-machine-arn" href="#aws-step-functions-state-machine-arn">`aws.step_functions.state_machine.arn`</a> | string | The ARN of the AWS Step Functions State Machine. | `arn:aws:states:us-east-1:123456789012:stateMachine:myStateMachine:1` | ![Development](https://img.shields.io/badge/-development-blue) |
