pipeline {
   agent any
   stages{
       stage('git clone'){
           steps{
              git credentialsId: '627d81ae-5ed6-471b-afc8-90c69fadd554', url: 'https://github.com/devops-surya/SampleMavenProject.git' 
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
       stage('publish junit test reports'){
           steps{
              junit 'target/surefire-reports/*.xml'
           }
           
       }

   }
}
