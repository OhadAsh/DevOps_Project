node('master') {
  stage('Checkout') {
    checkout scm
  }
  stage('Build project') {
   bat 'mvn package'
  }
  stage('Deploy') {
    if (env.BRANCH_NAME == 'master') {
      bat 'copy target\\OhadSaharReutF.war "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps\\OhadSaharReutF.war" '
    }
  }
}
