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
                bat '"C:\\Users\\kanch\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install --upgrade pip'
                bat '"C:\\Users\\kanch\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run App') {
            steps {
                bat '"C:\\Users\\kanch\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
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
