pipeline {
   agent any
   stages{
       stage('git clone'){
           steps{
               git 'https://github.com/supanja/sample.git' 
           }        
       } 
       stage('build the code'){
           steps{
              sh 'mvn package'
           }
       }
       stage('archive the artifacts'){
           steps{
              archive 'target/*.jar'
           }          
       }
       stage('publish the junit reports'){
           steps{
              junit 'target/surefire-reports/*.xml'
           }
           
       }

   }
}
