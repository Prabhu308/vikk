pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Prabhu308/vijay.git'
            }
        }
        stage('Compile') {
            steps {
                bat 'javac work.java'
            }
        }
        stage('Run Application') {
            steps {
                bat 'java work'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}