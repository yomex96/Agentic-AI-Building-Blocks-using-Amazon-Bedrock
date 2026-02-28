AWS Facilitated Event Setup
Perfect! You're attending an AWS-hosted workshop with pre-configured resources. Let's get your environment ready in just a few minutes.

Step 1: Access Your VS Code Online IDE
Find your VS Code URL in the workshop landing page provided by your facilitator
Open the URL in your browser
Open a terminal in VS Code (Terminal → New Terminal)
You should now see a VS Code interface with a terminal at the bottom.

Step 2: Set Up Your Python Environment
In your VS Code terminal, run these commands:

1
2
3
4
5
6
7
8
9
10
11
# Create a new directory for our workshop
mkdir agentic-ai-workshop
cd agentic-ai-workshop

# Create a Python virtual environment
python -m venv .venv

# Activate the virtual environment
source .venv/bin/activate

# You should see (.venv) in your terminal prompt now

Step 3: Install Dependencies
Create a requirements file and install packages:

1
2
3
4
5
6
7
8
9
10
# Create requirements.txt file
cat > requirements.txt << EOF
boto3>=1.34.0
streamlit>=1.28.0
requests>=2.31.0
Pillow>=10.0.0
EOF

# Install all dependencies
pip install -r requirements.txt

This will take a minute or two to download and install all the packages.

Step 4: Verify Your Setup
Test that everything is working:

1
2
3
4
5
6
7
8
# Test Python and boto3
python -c "import boto3; print('✅ boto3 installed successfully')"

# Test Streamlit
python -c "import streamlit; print('✅ Streamlit installed successfully')"

# Test AWS credentials (should show your account info)
aws sts get-caller-identity

You should see output showing your AWS account details. If you get an error, ask your workshop facilitator for help.

🔧 Troubleshooting
"AWS credentials not found"
Ask your workshop facilitator - credentials should be pre-configured
Virtual environment issues
In your VS Code terminal, run these commands:

1
2
3
# If activation fails, try:
python -m venv --clear .venv
source .venv/bin/activate

Package installation fails
In your VS Code terminal, run these commands:

1
2
3
# Try upgrading pip first
pip install --upgrade pip
pip install -r requirements.txt

✅ Setup Complete!
You should now have:

✅ VS Code Online IDE running
✅ Python virtual environment activated (you'll see (.venv) in your prompt)
✅ All required packages installed
✅ AWS credentials configured and tested
✅ Claude 4.5 Sonnet access enabled (enabled by default in an AWS facilitated event)
✅ Working directory created (agentic-ai-workshop)
Perfect! Your environment is ready. Let's move on to understanding how our AI agent architecture works! 🏗️
