node{
stage('SCM'){
git 'https://github.com/Java-Project-03-9AM/SpringMVCFormApp.git'
}
stage('building'){
  def mvn=tool name: 'MAVEN_HOME', type: 'maven'
  sh "${mvn}/bin/mvn package"
}
}
