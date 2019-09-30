pipeline {
    agent any
    stages {
        stage('Preparation') {
            steps{
                 
                 git credentialsId: '6f42db78-07d5-4143-afcb-f89fe2e7bf71', url: 'https://github.com/dyzwj/helloworld.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
                source '~/.bash_profile'
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
