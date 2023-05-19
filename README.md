# aws_s3_interview_preparation

here we go !!

## Theorical Questions Section

### Theorical Question 1

Do you know what storage classes is in s3

<details><summary><b>Answer</b></summary>
Amazon S3 offers a range of storage classes designed for different use cases. For example, you can store mission-critical production data in S3 Standard for frequent access, save costs by storing infrequently accessed data in S3 Standard-IA or S3 One Zone-IA, and archive data at the lowest costs in S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval, and S3 Glacier Deep Archive.

You can store data with changing or unknown access patterns in S3 Intelligent-Tiering, which optimizes storage costs by automatically moving your data between four access tiers when your access patterns change. These four access tiers include two low-latency access tiers optimized for frequent and infrequent access, and two opt-in archive access tiers designed for asynchronous access for rarely accessed data.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
</details>


### Theorical Question 2

storage lifecycle

<details><summary><b>Answer</b></summary>
It is a feature for transitioning objects in s3 storage clases and expiring them (deleting them) depending on an amount of time like after 30 days or a year
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
</details>

### Theorical Question 3

Do you know what is the object lock

<details><summary><b>Answer</b></summary>
Prevent Amazon S3 objects from being deleted or overwritten for a fixed amount of time or indefinitely. You can use Object Lock to help meet regulatory requirements that require write-once-read-many (WORM) storage or to simply add another layer of protection against object changes and deletions.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
</details>

### Theorical Question 4

Do you know what s3 batch job is

<details><summary><b>Answer</b></summary>
A batch job performs a specified operation on every object that is included in its manifest. A manifest lists the objects that you want a batch job to process and it is stored as an object in a bucket. You can use a comma-separated values (CSV)-formatted Amazon S3 Inventory report as a manifest, which makes it easy to create large lists of objects located in a bucket. You can also specify a manifest in a simple CSV format that enables you to perform batch operations on a customized list of objects contained within a single bucket.

After you create a job, Amazon S3 processes the list of objects in the manifest and runs the specified operation against each object. While a job is running, you can monitor its progress programmatically or through the Amazon S3 console. You can also configure a job to generate a completion report when it finishes. The completion report describes the results of each task that was performed by the job. 
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
</details>

### Theorical Question 5

Do you know what the s3 block access do

<details><summary><b>Answer</b></summary>
When Amazon S3 receives a request to access a bucket or an object, it determines whether the bucket or the bucket owner's account has a block public access setting applied. If the request was made through an access point, Amazon S3 also checks for block public access settings for the access point. If there is an existing block public access setting that prohibits the requested access, Amazon S3 rejects the request.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html
</details>

### Theorical Question 6

Do you know what the s3 bucket policy is

<details><summary><b>Answer</b></summary>
 Use IAM-based policy language to configure resource-based permissions for your S3 buckets and the objects in them.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
</details>

### Theorical Question 7

s3 access point

<details><summary><b>Answer</b></summary>
Amazon S3 access points simplify data access for any AWS service or customer application that stores data in S3. Access points are named network endpoints that are attached to buckets that you can use to perform S3 object operations, such as GetObject and PutObject. Each access point has distinct permissions and network controls that S3 applies for any request that is made through that access point.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
</details>

### Theorical Question 8

Do you know what Access control lists (ACLs) and se object ownership is ?

<details><summary><b>Answer</b></summary>
Grant read and write permissions for individual buckets and objects to authorized users. As a general rule, we recommend using S3 resource-based policies (bucket policies and access point policies) or IAM user policies for access control instead of ACLs. Policies are a simplified and more flexible access control option. With bucket policies and access point policies, you can define rules that apply broadly across all requests to your Amazon S3 resources.

S3 Object Ownership is an Amazon S3 bucket-level setting that you can use to disable or enable ACLs. By default, ACLs are disabled. With ACLs disabled, the bucket owner owns all the objects in the bucket and manages access to data exclusively by using access-management policies.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
</details>

### Theorical Question 9

Do you know what the s3 analizer is ?

<details><summary><b>Answer</b></summary>
Evaluate and monitor your S3 bucket access policies, ensuring that the policies provide only the intended access to your S3 resources.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
</details>


### Theorical Question 10

Do you know what the s3 object lambda ?

<details><summary><b>Answer</b></summary>
With Amazon S3 Object Lambda, you can add your own code to Amazon S3 GET, LIST, and HEAD requests to modify and process data as it is returned to an application. You can use custom code to modify the data returned by S3 GET requests to filter rows, dynamically resize and watermark images, redact confidential data, and more. You can also use S3 Object Lambda to modify the output of S3 LIST requests to create a custom view of all objects in a bucket and S3 HEAD requests to modify object metadata such as object name and size. You can use S3 Object Lambda as an origin for your Amazon CloudFront distribution to tailor data for end users, such as automatically resizing images, transcoding older formats (like from JPEG to WebP), or stripping metadata. 
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/transforming-objects.html
</details>

### Theorical Question 11

Do you know what the s3 event notifications are ?

<details><summary><b>Answer</b></summary>
You can use the Amazon S3 Event Notifications feature to receive notifications when certain events happen in your S3 bucket. To enable notifications, add a notification configuration that identifies the events that you want Amazon S3 to publish. Make sure that it also identifies the destinations where you want Amazon S3 to send the notifications. You store this configuration in the notification subresource that's associated with a bucket.

Amazon S3 event notifications are designed to be delivered at least once. Typically, event notifications are delivered in seconds but can sometimes take a minute or longer.
</details>

<details><summary><b>Source</b></summary>
https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html
</details>