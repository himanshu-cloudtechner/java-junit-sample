pipeline {
    tools {maven "My_Maven"}
    agent any
    stages {
        stage("compile") {
            steps {
                sh 'mvn clean install'
              }
            }
        stage('package') {
        steps {
                sh "mvn package"
        }
             }
 
 

        stage('Unit Test') {
            steps {
                sh "mvn test" 

            }
    

       post {

       always {    

       junit allowEmptyResults: true, testResults : 'target/*.xml'



               }
                }


             }





     
     }

 

     }
