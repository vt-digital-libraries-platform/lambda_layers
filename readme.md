# Introduction
This repositoy contains all the custom Lambda layer for VTDLP projects

# List of custom Lambda layer 
1. [noid-layer](noid-layer): Contains noid-mint and panda Python libraries.

# Create a Lambda layer
* Create a Lambda layer using CLI
```
cd iawa-layer
aws lambda publish-layer-version --layer-name noid-layer --description "NOID layer" --zip-file fileb://iawa-layer.zip --compatible-runtimes python3.7
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
