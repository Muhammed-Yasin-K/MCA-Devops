pipeline {
    agent any

    stages {

        stage('Setup Python Environment') {
            steps {
                bat '''
                "C:\\Users\\ASUS\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" --version

                "C:\\Users\\ASUS\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m venv venv

                call venv\\Scripts\\activate

                pip install --upgrade pip

                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                call venv\\Scripts\\activate

                pytest
                '''
            }
        }
    }
}
