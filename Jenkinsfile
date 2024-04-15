pipeline {
    agent any
    tools { 
        maven 'mvn3' 
        jdk 'java17' 
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/devops2301/loan.git']])
            }
        }
        stage('mvn clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('mvn package') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('mvn deploy') {
            steps {
                sh 'mvn deplo'
            }
        }
        stage('mvn sonar') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.login=squ_74b672131ba6ee29a315d2a956baacb53078f817'
            }
        }
    }
}
