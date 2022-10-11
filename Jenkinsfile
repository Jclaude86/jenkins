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
def qg = waitForQualityGate()
  }
   
