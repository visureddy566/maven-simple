pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "clean compile"
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
