# AWS-Labs_Foundation
## Lab5__Q1 
## Flow 
![Screenshot 2023-03-27 025217](https://user-images.githubusercontent.com/128603198/227816451-7f9e5918-fd49-4f3f-97f3-23e563c8dad0.png)

## Code
``` python
import boto3

def lambda_handler(event, context):
    # TODO implement
    s3 = boto3.client('s3')
    
    s3.upload_file(
        Filename="./anubis.txt",
        Bucket="targetbucket98",
        Key= "mustafa",
    )
    return None

```
![Code](https://user-images.githubusercontent.com/128603198/227816478-5adee4c6-ddd4-4bea-abfe-f2a529b9eca9.png)

## Trigger 
![Trigger](https://user-images.githubusercontent.com/128603198/227816498-4a230522-0ece-4326-8a9a-27fbd7360fe5.png)

## Video
https://user-images.githubusercontent.com/128603198/227816941-e7a29538-17e3-46ce-90ec-c5c497495e1a.mp4



