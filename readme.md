# Introduction
This repositoy contains all the custom Lambda layer for VTDLP projects

## List of custom Lambda layer
1. [Noid-mint Lambda layer](noid-layer): Contains noid-mint and panda Python libraries.
    * You can deploy this Lambda layer through [Serverless Application Repository - Noid-mint](https://console.aws.amazon.com/lambda/home?region=us-east-1#/create/app?applicationId=arn:aws:serverlessrepo:us-east-1:909117335741:applications/Noid-mint)

## Create a Lambda layer
* Create a Lambda layer using AWS CLI
    ```
    aws lambda publish-layer-version --layer-name noid-layer --description "NOID layer" --zip-file fileb://noid-layer.zip --compatible-runtimes python3.7
    ```
    Output
    ```
    {
        "Content": {
            "Location": "....",
            "CodeSha256": "xxxxxxxx+LyoETfaKSxxxxxxx",
            "CodeSize": 31585176
        },
        "LayerArn": "arn:aws:lambda:us-east-1:xxxx:layer:noid-layer",
        "LayerVersionArn": "arn:aws:lambda:us-east-1:xxxx:layer:noid-layer:1",
        "Description": "NOID layer",
        "CreatedDate": "2020-02-12T03:32:10.694+0000",
        "Version": 1,
        "CompatibleRuntimes": [
            "python3.7"
        ]
    }
    ```
