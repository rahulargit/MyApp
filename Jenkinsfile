pipeline {
    agent any

    environment {
        PYTHON_VENV = 'venv'
    }

    stages {
        stage('Clone MyApp') {
            steps {
                git 'https://github.com/rahulargit/MyApp.git'
            }
        }

        stage('Install Python Dependencies') {
            steps {
                bat 'python -m venv venv'
                bat '.\\venv\\Scripts\\pip install -r requirements.txt'
            }
        }

        stage('Deploy MyApp') {
            steps {
                bat 'pm2 restart MyApp || pm2 start .\\venv\\Scripts\\python.exe --name MyApp -- app.py'
            }
        }
    }
}
