# AWS New VPC
This stack will take multiple options as input where based on the inputs, it will create additional resources utilizing conditions.

Assumptions:
- Taken into consideration, its a main VPC where different products are included, so kept the default CIDR block large but if we want to split different products into their own vpc, we need to adjust the CIDR blocks appropriately.
- To communicate with S3, included a resource to create endpoint so that communication can be internal.
- flow logs into cloudwatch so that they can pushed to centralised AWS account( security account ) or ELK ( for longer storage )
- Not included the next step of pushing logs from cloudwatch to another AWS account or ELK, which can achieved by lambda or dedicated EC2 instance.
- seperate the application from VPC stack to reduce any future changes blast radius.
