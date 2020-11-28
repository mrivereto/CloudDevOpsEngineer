# CloudFormation

A **Stack** is a collection of resources that gets created from the script.

## Command to create the stack

```
aws cloudformation create-stack --stack-name <name of stack> --region <choose a region> --template-body file://<your yaml or json file>
```

__Output:__
```
{
    "StackId": "arn:aws:cloudformation:us-west-2:559761644045:stack/myfirsttest/86c37860-3164-11eb-8af5-0a8688021207"
}
```

**StackId** is your stack identifier, you use this ID to check the status with AWS CLI.

## Command to update the stack
```
aws cloudformation update-stack --stack-name <name of stack> --region <choose a region> --template-body file://<your yaml or json file>
```

If you try to use create-stack command you will get an error like:
```
An error occurred (AlreadyExistsException) when calling the CreateStack operation: Stack [myfirsttest] already exists
```