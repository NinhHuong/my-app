pipeline {
    agent any
    tools { 
        maven 'maven-3.5.4' 
        jdk 'jdk-1.8' 
    }
    stages {
        stage('Example clean') {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/NinhHuong/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage('Example install') {
            steps {
                sh "mvn install -f my-app"
            }
        }
        stage('Example test') {
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Example package') {
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}

