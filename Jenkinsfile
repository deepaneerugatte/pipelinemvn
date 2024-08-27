node{
stage('SCM'){
git 'https://github.com/Java-Project-03-9AM/SpringMVCFormApp.git'
}
stage('building artifact'){
  def mvn=tool name: 'MAVEN_HOME', type: 'maven'
  sh "${mvn}/bin/mvn package"
}
 /* stage('email notification'){
    mail bcc: '', 
     body: '''HI Deepa,
     This to mention that your job ran successfully!!
     ThANKS,
     JD''', cc: 'ndeepa5227@gmail.com', from: '', replyTo: '', subject: 'Job triggered', to: 'deeparamya532@gmail.com'
  } */
  stage('slack notification'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
    channel: '#jenkins', 
    color: 'good', 
    message: 'hi Baby , build triggered successfully!!', 
    notifyCommitters: true, teamDomain: 'JENKINS_PROJECT', 
    tokenCredentialId: 'slack_token', 
    username: 'deeparamya532@gmail.com'
  }
}
