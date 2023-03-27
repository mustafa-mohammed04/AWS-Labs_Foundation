# AWS-Labs_Foundation
#### Lab 5 Q2

## Flow 
![Flow](https://user-images.githubusercontent.com/128603198/228052224-860251b4-214c-42bf-a758-8e5de560d474.png)

## Trigger
![Trigger](https://user-images.githubusercontent.com/128603198/228063168-9c54422f-eb65-458d-a797-f0776fe26450.png)


## Code 
``` python
import boto3

s3 = boto3.resource('s3')

def lambda_handler (event, context):
    bucket = s3.Bucket('mustafasrc98')
    dest_bucket=s3.Bucket('mustafadest98')

    print(dest_bucket)
    print(bucket)
 
    for obj in bucket.objects.all():
        dest_key=obj.key
        print(dest_key)
        s3.Object(dest_bucket.name, dest_key).copy_from(CopySource= {'Bucket': obj.bucket_name, 'Key': obj.key})
```

## Video
https://user-images.githubusercontent.com/128603198/228062300-bf6ab39a-0689-4a33-8622-d4afd0a5616b.mp4



