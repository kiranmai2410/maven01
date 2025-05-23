pipeline {
    agent any

    tools {
        maven 'maven 3.6.3'
        jdk 'jdk-23'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/kiranmai2410/maven01.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
