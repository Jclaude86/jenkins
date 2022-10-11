
   
  
    
    
  
pipeline{
 ageny any 
 stages{
     stage ('checkout'){
         steps
         { git branch: 'dev', url: 'https://github.com/Jclaude86/jenkins.git'
             
         }
     }
     stage('sonarQube Analysis'){
       steps{ sh 'mvn sonar:sonar'
           
       }  
     }
     stage('Quality gate'){
         steps{ waitForQualityGate abortPipeline: true
             
         }
     }
 }
}











  
 
    
   
