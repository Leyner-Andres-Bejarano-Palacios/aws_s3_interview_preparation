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