pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "M3"
   }

   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            sh "mvn -Dmaven.test.failure.ignore=true clean compile"
         }
         }
      stage("Test") {
          steps {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'  
            sh "mvn -Dmaven.test.failure.ignore=true clean test"
            
          }

      }
      stage("Deploy") {
          steps {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'  
            sh "mvn -Dmaven.test.failure.ignore=true clean install"
            sh "java -cp target/simple-maven-project-with-tests-1.0-SNAPSHOT.jar com.github.jitpack.App"
            
          }
          post {
              success {
                  archiveArtifacts 'target/*.jar'
              }

          }


      }

      }
   }

