pipeline {
    agent any

    tools {
        maven 'maven_3.6.3'  // Ensure this matches your Jenkins Maven installation name
        jdk 'jdk-21'         // Ensure this matches your Jenkins JDK tool name or installed JDK
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
