Project Overview

This project demonstrates a complete CI/CD pipeline for a Flask application using Jenkins.
The pipeline automates the process of pulling code from GitHub, installing dependencies, running tests, and validating the application.

**Tech Stack**
**Python (Flask)
Jenkins
Git & GitHub
Pytest (for testing)**

**Project Structure**
flask-cicd-assignment/
│
├── app.py                # Flask application
├── requirements.txt     # Project dependencies
├── test_app.py          # Unit tests
├── Jenkinsfile          # CI/CD pipeline definition
├── README.md            # Project documentation

<img width="940" height="700" alt="image" src="https://github.com/user-attachments/assets/a153bc7d-af93-4dfd-8b81-f346098e4ac5" />



**CI/CD Pipeline Stages**
1️- Checkout Code
Jenkins pulls the latest code from GitHub repository.
2️- Install Dependencies
Installs required Python packages using:
pip3 install --break-system-packages -r requirements.txt
3️- Run Tests
Executes unit tests using pytest:
python3 -m pytest
4️- Run Application (Validation)
Validates Flask app using:
python3 -c "import app"


**Testing**
Testing is done using pytest
Ensures application functionality before deployment

<img width="1647" height="496" alt="image" src="https://github.com/user-attachments/assets/c5215204-ae4f-4a24-880e-c3aea0ba135e" />


**How to Run Locally**
Step 1: Clone Repo
git clone https://github.com/<your-username>/flask-cicd-assignment.git
cd flask-cicd-assignment
Step 2: Install Dependencies
pip install -r requirements.txt
Step 3: Run Application
python app.py


**Challenges Faced & Solutions**
Git authentication failed, which was resolved by using a GitHub Personal Access Token instead of a password
Branch mismatch issue (master vs main) was fixed by updating the Jenkins configuration
Python restricted environment issue was handled using the --break-system-packages option
pytest not found error was resolved by running it using python -m pytest
Flask app was blocking the pipeline, which was fixed using timeout or import-based execution
Port already in use issue was handled by avoiding running a persistent server during pipeline execution


**Key Learnings**
Implemented end-to-end CI/CD pipeline
Understood Jenkins pipeline stages
Handled real-world DevOps issues
Learned debugging in CI environments


**Future Enhancements**
Dockerize the application
Deploy to AWS/Azure
Add monitoring & logging
Integrate with Kubernetes


**Author
Madhu Singh**

**Conclusion

This project showcases a real-world CI/CD pipeline implementation, demonstrating practical DevOps skills including automation, testing, and troubleshooting.
**

