pipeline {
    agent any

    tools {
        maven 'maven 3.6.3'    // Use the name configured in Jenkins
        jdk 'jdk-23'           // Use the correct JDK name configured
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/kiranmai2410/maven01.git'
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
