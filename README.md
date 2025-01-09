# Hosting-simple-static-web-site-in-EC2
Step 1: Launch an EC2 Instance
Log in to AWS Management Console.
Navigate to EC2 → Instances → Launch Instances.
Configure the instance:
  - AMI: Choose Amazon Linux 2 AMI (recommended for beginners).
  - Instance Type: Select t2.micro (Free Tier eligible).
  - Key Pair: Create or choose an existing key pair.
Network Settings:
  - Select an existing security group or create a new one.
  - Ensure the security group allows inbound HTTP (port 80) and SSH (port 22) traffic.
Launch the instance.
Step 2: Connect Using EC2 Instance Connect
Once the instance is running, select it in the Instances list.
Click Connect in the top-right corner of the AWS Console.
Choose the EC2 Instance Connect tab and click Connect. This will open a browser-based terminal session to your EC2 instance.
Step 3: Install and Configure Apache HTTP Server
Update the instance:
  - sudo yum update -y
Install the Apache web server:
  - sudo yum install httpd -y
Start the Apache server:
  - sudo systemctl start httpd
Enable the server to start on boot:
  - sudo systemctl enable httpd
Step 4: Upload Your HTML and CSS Files
1: Use the Terminal
  - Create the website files directly on the server:
    - Create an index.html file:
      - sudo nano /var/www/html/index.html
      - Add your HTML content, then save and exit (Ctrl + O, Enter, Ctrl + X).
    - Repeat for style.css or other files if needed.
    - Ensure the files are in /var/www/html:
      - sudo mv /path/to/your/files /var/www/html/
Step 5: Accessing it using public ip
-	Access it using public ip that is there in ec2.

