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
        stage('Run Tests') {
            steps {
                // Assuming you have a test class named WorkTest
                bat 'java -cp . org.junit.runner.JUnitCore WorkTest'
            }
        }
        stage('Run Application') {
            steps {
                bat 'java work'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
        always {
            echo 'Pipeline finished.'
        }
    }
}