---
template: post
title: 2019 AWS Certified Solutions Architect — Associate Exam Preparation
slug: aws-certified-solutions-architect-associate
draft: false
date: 2019-10-15T16:00:00.000Z
description: >-
  I passed the AWS Certified Solutions Architect - Associate (SAA-C01) exam in
  Oct 2019 after spending 1 month to prepare for the exam. Here are my study
  plan and exam tips.
category: AWS
tags:
  - AWS Certified Solutions Architect
  - AWS Exam
  - Exam tips
  - SAA-C01
---
I passed the [AWS Certified Solutions Architect — Associate (SAA-C01) exam](https://aws.amazon.com/certification/certified-solutions-architect-associate/) in Oct 2019 after spending 1 month to prepare for the exam. Here are my study plan and exam tips.



![aws certified](/media/aws-certified-logo_color-horz_360x60.png "AWS ertified LogoC")

![aws solution architect associate](/media/solutions-architect-associate-tag_360x32.png "AWS Solution Architect Associate Tag")



### **My Background**

I am a finance graduate with some coding experiences, with no prior knowledge before taking the exam.

### **Exam Information**

Number of questions: **~ 65**\
Time limit: **130 minutes**\
Question types: **Multiple choice, Multiple response**\
Score range: **100 - 1000**\
Minimum passing score: **720**

The Five Domains of the exam:

1. Design Resilient Architectures: 34%
2. Define Performant Architectures: 24%
3. Specify Secure Applications and Architectures: 26%
4. Design Cost-Optimized Architectures: 10%
5. Define Operationally Excellent Architectures: 6%

Reference: [AWS Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS_Certified_Solutions_Architect_Associate-Exam_Guide_EN_1.8.pdf)

### **Study Plan**

For the **first 2 weeks**, the focus is on getting yourself familiar with different AWS services. Learn the theory by taking online course. Create an AWS account and start exploring the products with [Free Tier](https://aws.amazon.com/free).

To better understand the [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/), I recommend taking the free [Exam Readiness course](https://www.aws.training/Details/Curriculum?id=20685) offered by [AWS Digital and Classroom Training](https://aws.amazon.com/training/course-descriptions/). Remember to try out the [Sample Questions](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS_Certified_Solutions_Architect_Associate_Sample_Questions.pdf) as soon as possible to get a taste of the AWS exam.

For the **next 2 weeks**, try taking practice exams and revisiting the topics that you are not familiar with. Doing practice exams is really important as you must adapt yourself to different types of question. There are lots of tricky questions, don’t worry if you get less than 70% in the beginning. You are ready to go once you consistently get higher than 80%.

Side note: how I allocated my time:

* weekday: ~2.5 hrs/day
* weekend: ~4 hrs/day

### **List of Important Topics**

* IAM User, Group, Policy, Role
* EC2, EBS, EFS
* Elastic Load Balancer, Auto Scaling Group
* RDS, DynamoDB, Aurora
* VPC, VPN, Direct Connect, VPC endpoints
* Route53
* S3
* SQS, SNS, SWF, Step Functions
* CloudFront, ElastiCache, DAX
* Cloud Formation, Elastic Beanstalk
* CloudWatch, CloudTrail
* API Gateway, Lambda
* Others: ECS, Snow, Storage Gateway, Redshift…

### Useful Courses and Resources

**Linux Academy**: [SAA Course](https://linuxacademy.com/course/aws-certified-solutions-architect-2019-associate-level/)

* Detailed walk through on different AWS services, great for building foundation
* Total of 45 hours, you can learn at your own pace
* Taught by [Adrian Cantrill](https://www.linkedin.com/in/adriancantrill/?originalSubdomain=au)

**Udemy**: [SAA Practice Exams](https://www.udemy.com/course/aws-certified-solutions-architect-associate-amazon-practice-exams/)

* Scenario-based Solutions Architect questions
* 6 sets of practice tests, each with 65 unique questions
* Simulates actual exam environment
* Has full explanation to each question

**AWS Digital and Classroom Training**: [Exam Readiness: SAA (Digital)](https://www.aws.training/Details/Curriculum?id=20685)

* Reviews sample exam questions in each topic area
* Teaches you how to interpret the concepts being tested so that you can easily eliminate incorrect responses.
* Total of 2 hours

**FAQs**(optional): [EC2](https://aws.amazon.com/ec2/faqs/), [VPC](https://aws.amazon.com/vpc/faqs/), [RDS](https://aws.amazon.com/rds/faqs/), [S3](https://aws.amazon.com/s3/faqs/), [Route53](https://aws.amazon.com/route53/faqs/)

* To consolidate your knowledge

### **What’s on my exam**

There were quite a lots of database related questions, particularly on DynamoDB. Load Balancing and Auto scaling played an important part as well. New services like Athena also appeared in my exam.

I hope you find this article helpful! 🎉
