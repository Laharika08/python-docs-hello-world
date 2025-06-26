pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Laharika08/python-docs-hello-world.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Use virtualenv optionally if needed
                sh 'python3 -m pip install --upgrade pip'
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run App') {
            steps {
                sh 'python3 app.py &'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully.'
        }
        failure {
            echo '❌ Pipeline failed. Please check the logs.'
        }
    }
}
