node('built-in') 
{
   
stage('continuous donwload')
  {
   git branch: 'dev', url: 'https://github.com/Jclaude86/jenkins.git'
 }
    
   stage('continuous build')
   {
    sh 'mvn package'
    } 
    
   
