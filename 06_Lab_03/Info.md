
# Contents / Commands

- CIDR to IP Range Conversion
    - https://www.ipaddressguide.com/cidr

- Key Pair
    - gl-lab-03

- Upload the file
    - Change Permission
        - chmod 400 ./gl-lab-03.pem
    - Using SCP to upload the files
        - scp -i ./gl-lab-03.pem -r ./GL-AWS-Lab-03.zip ec2-user@3.93.188.2:~

- Verify the Upload Operation
    - SSH Connect to EC2
        - ssh -i ./gl-lab-03.pem ec2-user@3.93.188.2

- Unzip the uploaded Zip file
    - unzip ./GL-AWS-Lab-03.zip
    
- Supply permission to EC2 instance
    - aws configure

    - Details
        - AWS Access Key ID : 
            - Refer 'accessid' in the Nuvepro Console
        - AWS Secret Access Key : 
            - Refer 'accesskey' in the Nuvepro Console
        - Default Region: us-east-1
        - Default output format : json

- Execute the CF files
    - CF1.json
        - aws cloudformation create-stack --stack-name gl-lab-03-stack --template-body file://./CF-Template-Files/v2-Work/CF1.json

    - CF2.json
        - aws cloudformation create-stack --stack-name gl-lab-03-stack --template-body file://./CF-Template-Files/v2-Work/CF2.json


- Screenshots

    - Screenshot #1
        - Response of the CF create stack command with CF1.json

    - Screenshot #2
        - Response of the CF create stack command with CF2.json
        
    - Screenshot #3
        - Events log of CF showing security group name as 'WebServerSecurityGroup'

    - Screenshot #4
        - Response from EC2 Server 1

    - Screenshot #5
        - Response from EC2 Server 2
        



