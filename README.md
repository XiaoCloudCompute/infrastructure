# Infrastructure

## Useful reference
- [AWS cloud Formation User Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [AWS cli User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)


## Common command

- specify profile
```shell
export AWS_PROFILE=dev
```

- create stack
```shell
aws cloudformation create-stack --stack-name my-vpc --template-body file://CloudFormation/csye6225-infra.yml
```

- delete stack
```shell
aws cloudformation delete-stack --stack-name my-vpc
```