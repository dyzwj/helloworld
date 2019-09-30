pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '500378f5-a6e4-4255-984e-61537fe0e455', url: 'git@gitlab.aniu.so:aniu-yunwei/game-of-life.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
                sh 'mvn test' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
                sh 'mvn clean deploy'
            }
        }
    }
}
