node('built-in') 
{
   
stage('continuous donwload')
  {
   git branch: 'dev', url: 'https://github.com/Jclaude86/jenkins.git'
 }
    stage('sonarQube Analysis') {
   sh 'mvn sonar:sonar'
}
 stage("Quality Gate"){
  timeout(time: 1, unit: 'HOURS') {
def qg = waitForQualityGate()
if (qg.status != 'OK') {
error "Pipeline aborted due to quality gate failure: ${qg.status}"
              }
          }
      } 
    sh 'mvn package'
    } 
    
   stage('continuous deployment')
   {
   deploy adapters: [tomcat8(credentialsId: 'dev', path: '', url: 'http://172.31.80.96:8080')], contextPath: 'qaenv', war: '**/*.war'
   }   
    
}
