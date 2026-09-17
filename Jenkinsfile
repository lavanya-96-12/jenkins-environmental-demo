pipeline {
    agent any

    environment {
        APP_NAME = 'GradeBookApp'
        APP_VERSION = '1.0.0'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/lavanya-96-12/jenkins-environment-demo.git'
            }
        }

        stage('Show App Info') {
            steps {
                echo "Building ${env.APP_NAME}, version ${env.APP_VERSION}"
            }
        }

        stage('Build') {
            steps {
                bat 'C:\\Users\\lavan\\AppData\\Local\\Programs\\Python\\Python314\\python.exe -m py_compile app.py'
                echo "${env.APP_NAME} version ${env.APP_VERSION} compiled successfully."
            }
        }
    }
}
