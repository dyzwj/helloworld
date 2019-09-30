pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout'
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
