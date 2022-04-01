# Infrastructure

## Useful reference
- [AWS cloud Formation User Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [AWS cli User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)


## Common command

- specify profile
```shell
export AWS_PROFILE=dev
```

- create git user stack
```shell
aws cloudformation create-stack --stack-name gituser --template-body file://CloudFormation/csye6225-infra-for-github.yml --capabilities CAPABILITY_NAMED_IAM --profile=demo
```

- create stack
```shell
aws cloudformation create-stack --stack-name my-vpc --parameters ParameterKey=ImageId,ParameterValue=ami-0a432917e909fea81 --template-body file://CloudFormation/csye6225-infra.yml --capabilities CAPABILITY_NAMED_IAM --profile=demo
```

- delete stack(rm bucket objects at first)
```shell
aws s3 rm s3://bucket-name --recursive --profile=demo
aws cloudformation delete-stack --stack-name my-vpc --profile=demo
```