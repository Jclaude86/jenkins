node
{
   
stage('continuous donwload')
  {
   git branch: 'dev', url: 'https://github.com/Jclaude86/jenkins.git'
 }
   stage('sonarQube Analysis')
  {
   sh 'mvn sonar:sonar'
 } 
   
  
    
    
  
} 
    
   
