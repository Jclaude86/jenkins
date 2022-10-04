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
    
   stage('continuous deployment')
   {
   deploy adapters: [tomcat8(credentialsId: 'dev', path: '', url: 'http://172.31.80.96:8080')], contextPath: 'qaenv', war: '**/*.war'
   } 
    
    stage('continuous testing') 
    {
    echo 'testing has passed'
   }
    stage('continuous delivery') 
    { 
    deploy adapters: [tomcat8(credentialsId: 'prod', path: '', url: 'http://172.31.83.7:8080')], contextPath: 'prodenv', war: '**/*.war'
    }
  
    
}
