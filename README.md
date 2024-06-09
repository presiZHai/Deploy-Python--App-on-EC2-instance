## Deploy Python Apps on an EC2 Instance

### How to Deploy Streamlit and Other Python Apps on an EC2 Instance
1. Login to your AWS console and launch an EC2 instance
2. Run the following commands

### Note: Map the port to port 8501 for Streamlit, port 8080 for FastAPI, or as appropriate.

```bash
# Update package lists
sudo apt update
sudo apt-get update

# Upgrade all packages
sudo apt upgrade -y

# Install essential packages
sudo apt install git curl unzip tar make sudo vim wget -y

# Clone your repository
git clone "Your-repository"

# Install pip for Python 3
sudo apt install python3-pip

# Install the requests Python library using APT
sudo apt install python3-requests

# OR Create a virtual environment using venv
# Install venv
sudo apt install python3-venv

# Create a new virtual environment, .venv, in a directory
python3 -m venv .venv

# Activate the virtual environment 
source .venv/bin/activate

# Install requirements
pip3 install -r requirements.txt


# Temporary Running

python3 -m streamlit run app.py
# OR
python3 app.py

# Permanent running

nohup python3 -m streamlit run app.py &

```bash