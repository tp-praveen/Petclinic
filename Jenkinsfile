node {
  stage 'Build-Branch(praveen)'
  checkout scm
  sh 'mvn clean install -DskipTests'  
  sh 'which docker'  
  sh 'docker build -t "tomcat:petclinic" .'
  sh 'docker stop $(docker ps -a -q)'
  sh 'docker run -d -p 8084:8080 -e TOMCAT_PASS="mypass" tomcat:petclinic'  
}