pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "compile package"
                // 
            }
        }
        stage('Test') { 
            steps {
               sh "clean test"
                // 
            }
        }
        stage('Deploy') { 
            steps {
                sh "clean package"
                // 
            }
        }
    }
}
