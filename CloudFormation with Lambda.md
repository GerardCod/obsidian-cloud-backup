#Development #Lambda #CloudFormation 

According with the next scenario: Your company wants to move away from manually managing Lambda in the AWS console and wants to upload and update them using AWS CloudFormation.

How do you declare an AWS Lambda function in CloudFormation?

**Upload all the code as a zip to S3 and refer the object in `AWS::Lambda::Function` block**
-------------------------------------------------------------------------------
You can upload all the code as a zip to S3 and refer the object in `AWS::Lambda::Function` block.

The AWS::Lambda::Function resource creates a Lambda function. To create a function, you need a deployment package and an execution role. The deployment package contains your function code.

**Write the AWS Lambda code inline in CloudFormation in the `AWS::Lambda::Function` block as long as there are no third-party dependencies**
-------------------------------------------------------------------------------
The other option is to write the code inline for Node.js and Python as long as there are no dependencies for your code, besides the dependencies already provided by AWS in your Lambda Runtime (aws-sdk and cfn-response and many other AWS related libraries are preloaded via, for example, boto3 (python) in the lambda instances.)

YAML template for creating a Lambda function:

```yaml
Type: AWS::Lambda::Function
Properties:
  Code:
    Code
  DeadLetterConfig:
    DeadLetterConfig
  Description: String
  Environment:
    Environment
  FileSystemConfigs:
    - FileSystemConfig
  FunctionName: String
  Handler: String
  KmsKeyArn: String
  Layers:
    - String
  MemorySize: Integer
  ReservedConcurrentExecutions: Integer
  Role: String
  Runtime: String
  Tags:
    - Tag
  Timeout: Integer
  TracingConfig:
    TracingConfig
  VpcConfig:
    VpcConfig
```