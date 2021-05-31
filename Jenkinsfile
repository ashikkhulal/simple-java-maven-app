pipeline {
  agent any
   stages {
      stage ('Build') {
          steps{
              sh 'mvn clean install -DskipTests'
          }
      }
      stage ('Test') {
          steps {
              mvn test
              junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'
          }
      }
      stage ('Deploy') {
          steps {
             echo "Deploying to Dev environment" 
          }
      }
       
      }
      
   
   }
