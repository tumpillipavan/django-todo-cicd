pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/tumpillipavan/django-todo-cicd.git'
            }
        }

        stage('Build') {
            steps {
                dir('MavenHelloWorld-main') {
                    bat 'mvn clean package'
                }
            }
        }

        stage('Test') {
            steps {
                dir('MavenHelloWorld-main') {
                    bat 'mvn test'
                }
            }
        }
    }
}
