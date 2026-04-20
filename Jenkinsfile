pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git 'https://github.com/San05-git/c2.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}
