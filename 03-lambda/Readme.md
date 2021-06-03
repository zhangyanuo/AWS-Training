### **What is serverless?**
a cloud computing execution model in which the cloud provider allocates machine resources on demand, taking care of the servers on behalf of their customers.
https://en.wikipedia.org/wiki/Serverless_computing

***

### **Create lambda function with AWS Web Console and test**

*Output：*

>![Output](https://raw.githubusercontent.com/zhangyanuo/AWS-Training/master/03-lambda/img/Picture1.png)


### **Lambda function via aws cli with ZIP file and invoke Create Lambda**

`Question:想用自己的aws账户如何配置saml2aws？`

>`error authenticating to IdP: error following: request for url: https://ap-southeast-2.console.aws.amazon.com/idp/startSSO.ping?PartnerSpId=urn:amazon:webservice`

### **Create lambda by aws cloudformation**

>![lambda](https://raw.githubusercontent.com/zhangyanuo/AWS-Training/master/03-lambda/img/Picture2.png)
Output:
 >![output](https://raw.githubusercontent.com/zhangyanuo/AWS-Training/master/03-lambda/img/Picture3.png)
 
`Question:'sts:AssumeRole' 这个什么意思?`

### **Log lambda request event to cloudwatch：**

>![cloudwatcher](https://raw.githubusercontent.com/zhangyanuo/AWS-Training/master/03-lambda/img/Picture4.png)

`Question:为啥没有任何log在test之后？`

