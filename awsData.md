# AWS Data Engineer Question Answer

**1. A data engineer is configuring an AWS Glue job to read data from an Amazon S3 bucket. The data engineer has set up the necessary AWS Glue connection details and an associated IAM role. However, when the data engineer attempts to run the AWS Glue job, the data engineer receives an error message that indicates that there are problems with the Amazon S3 VPC gateway endpoint.
The data engineer must resolve the error and connect the AWS Glue job to the S3 bucket.
Which solution will meet this requirement?**

```
A. Update the AWS Glue security group to allow inbound traffic from the Amazon S3 VPC gateway endpoint.
B. Configure an S3 bucket policy to explicitly grant the AWS Glue job permissions to access the S3 bucket.
C. Review the AWS Glue job code to ensure that the AWS Glue connection details include a fully qualified domain name.
D. Verify that the VPC's route table includes inbound and outbound routes for the Amazon S3 VPC gateway endpoint.
```
<details>
  <summary>Click to See the Answer</summary>

✅ **Correct Answer: D – Verify Route Table Configuration**  

**Reason:**  
- VPC **gateway endpoints require proper route table entries** to function.  
- Route tables **must include S3 prefix lists** to direct traffic correctly.  
- Ensures **inbound & outbound routing** for S3 access via the gateway endpoint.  

</details>

**2. A retail company has a customer data hub in an Amazon S3 bucket. Employees from many countries use the data hub to support company-wide analytics. 
A governance team must ensure that the company's data analysts can access data only for customers who are within the same country as the analysts.
Which solution will meet these requirements with the LEAST operational effort?**

```
A. Create a separate table for each country's customer data. Provide access to each analyst based on the country that the analyst serves.
B. Register the S3 bucket as a data lake location in AWS Lake Formation. Use the Lake Formation row-level security features to enforce the company's access policies.
C. Move the data to AWS Regions that are close to the countries where the customers are. Provide access to each analyst based on the country that the analyst serves.
D. Load the data into Amazon Redshift. Create a view for each country. Create separate IAM roles for each country to provide access to data from each country.
 Assign the appropriate roles to the analysts.
```

<details>
  <summary>Click to See the Answer</summary>

✅ **Correct Answer: B Register the S3 bucket as a data lake location in AWS Lake Formation.**  

**Reason:**  
- Lowest operational effort as it uses built-in features
- Maintains single source of truth
- No data migration required
- Row-level security is precisely designed for this use case
- Native integration with S3
- Centralized governance and access control

</details>
