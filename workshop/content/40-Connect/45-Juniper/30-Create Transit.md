---
title: "Deploy Transit Gateway"
chapter: true
weight: 30
---

## Deploy Transit Gateway and Datacenter Router

We now are ready to start our connectivity and routing policy.
Run CloudFormation template 2.tgw-csr.yaml to deploy the Transit Gateway, route Tables, and the Datacenter Router (Cisco CSR).

1. Click on the CloudFormation Launch link below that corresponds to the AWS Region in which you deploy the first stack.

   [![US East (N. Virginia)](https://samdengler.github.io/cloudformation-launch-stack-button-svg/images/us-east-1.svg)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?stackName=tgw1-csr&templateURL=https://s3.amazonaws.com/net-workshop-us-east-1/2.tgw-csr.yaml&param_ParentStack=tgw1)

   [![US East (Ohio)](https://samdengler.github.io/cloudformation-launch-stack-button-svg/images/us-east-2.svg)](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/create/review?stackName=tgw1-csr&templateURL=https://s3.amazonaws.com/net-workshop-us-east-2/2.tgw-csr.yaml&param_ParentStack=tgw1)
   [![US West (Oregon)](https://samdengler.github.io/cloudformation-launch-stack-button-svg/images/us-west-2.svg)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?stackName=tgw1-cst&templateURL=https://s3.amazonaws.com/net-workshop-us-east-1/2.tgw-csr.yaml&param_ParentStack=tgw1)
   [![EU West (Ireland)](https://samdengler.github.io/cloudformation-launch-stack-button-svg/images/eu-west-1.svg)](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/create/review?stackName=tgw1-csr&templateURL=https://s3.amazonaws.com/net-workshop-us-east-1/2.tgw-csr.yaml&param_ParentStack=tgw1)
   [![EU West (Singapore)](https://samdengler.github.io/cloudformation-launch-stack-button-svg/images/ap-southeast-1.svg)](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/create/review?stackName=tgw1-csr&templateURL=https://s3.amazonaws.com/net-workshop-us-east-2/2.tgw-csr.yaml&param_ParentStack=tgw1)

1. For the **Specify stack details** give the stack a name (compounded names work well. i.e. if the VPC stack created in the setup module was named **TGW1** name this stack **TGW1-CSR**), pick the keypair you created earlier, and enter the name of your first stack (must be entered exactly to work). Click **Next**.
   ![Stack Parameters](/images/createStack-SRXparameters.png)

1. For **Configuration stack options** we dont need to change anything, so just click **Next** in the bottom right.

1. Scroll down to the bottom of the **Review name_of_your_stack** and check the **I acknowledge the AWS CloudFormation might create IAM resources with custom names.** Click the **Create** button in the lower right.
   ![Create Stack](/images/createStack-VPCiam.png)

1. wait for the Stack to show **Create_Complete**.
   ![Stack Complete](/images/createStack-SRXcomplete.png)
