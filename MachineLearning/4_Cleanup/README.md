# Clean up Instructions

**If you're running this inside of an Event Engine environment, you can stop reading.**

### CloudFormation

1. Navigate to your Cloud9 environment
1. Run the following commands to delete your resources:
    ```
    # Delete your bucket and all contents
    aws s3 rb s3://$bucket --force

    # Delete your queue if you made one manually
    aws sqs delete-queue --queue-url $queue_url

    # The inference resources from module 3
    aws cloudformation delete-stack --stack-name wildrydes-ml-mod3

    # The machine learning resources from module 2
    aws cloudformation delete-stack --stack-name wildrydes-ml-mod2

    # The data processing resources from module 1
    aws cloudformation delete-stack --stack-name wildrydes-ml-mod1
    ```
1. Exit your Cloud9 environment
1. Select the environment you've been using
1. Click **Delete**
1. Follow the directions

**CONGRATS!** You're done!

### ...OR CDK

1. Navigate to your Cloud9 environment
1. Run the following commands to delete your resources:
    ```
    # In real life, use the Force wisely...

    # Delete your bucket and all contents
    aws s3 rb s3://$bucket --force

    # Delete your queue if you made one manually
    aws sqs delete-queue --queue-url $queue_url

    # Tear everything down
    cdk destroy *Stack --force
    ```
1. Exit your Cloud9 environment
1. Select the environment you've been using
1. Click **Delete**
1. Follow the directions

**CONGRATS!** You're done!
