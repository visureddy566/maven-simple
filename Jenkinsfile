pipeline {
    agent any

    tools {
        maven "maven-3"
    }

    stages {
        stage ('Compile')
        steps {
            sh "mvn clean compile"
        }
        stages ('Test') {
            steps {
                sh "mvn clean test"
            }
        }
    }
}
