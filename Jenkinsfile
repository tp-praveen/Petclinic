node {
  stage 'Build-Master'  
  checkout scm
  sh 'mvn clean install -DskipTests'
  sh 'which docker'  
  sh 'docker build -t "tomcat:petclinic" .'
  sh 'docker stop $(docker ps -a -q)'
  sh 'docker run -d -p 8083:8080 -e TOMCAT_PASS="mypass" tomcat:petclinic'
}