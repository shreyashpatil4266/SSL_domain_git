# SSL_domain_git

this is the command used for coping all the data from the path provided to the server in website-temp then we ssh into the ec2 
scp -i ssl.pem -r "/c/Users/patil/OneDrive/Documents/WebisteTemp/templatemo_591_villa_agency" ec2-user@ec2-13-219-84-181.compute-1.amazonaws.com:/home/ec2-user/website-temp
ssh -i ssl.pem ec2-user@ec2-13-219-84-181.compute-1.amazonaws.com
cd ~/website-temp



# Check current git status
git status

# Stage all modified and new files
git add .

# Commit with a message
git commit -m "Initial commit with website files"

# Add remote GitHub repository
git remote add origin https://github.com/your-username/your-repo-name.git

# Push to GitHub (force if first time or error occurs)
git push -u origin main



# Install nginx (if not installed)
sudo yum install nginx -y   # For Amazon Linux/CentOS
# or
sudo apt install nginx -y   # For Ubuntu/Debian

# Start nginx
sudo systemctl start nginx

# Enable nginx to start on boot
sudo systemctl enable nginx

# Check nginx status
sudo systemctl status nginx



#SSL Certificate

# Install Certbot
sudo yum install certbot python3-certbot-nginx -y

#Obtain or renew certificate for your domains with Nginx plugin
sudo certbot --nginx -d shreyash.shop -d www.shreyash.shop


#Check certificates info
sudo certbot certificates


