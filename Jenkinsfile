node {
  stage 'Build-Master'  
  checkout scm
  echo 'maven clean install skipping tests'
  sh 'mvn clean install -DskipTests'
  echo 'stopping docker container if running'
  existing = sh '$(docker ps | grep tomcat:petclinic | grep -o "^[0-9a-z]*")'  
  echo existing
  //if [ ! -z "$existing" ]; then  
  //docker stop $existing
  //fi
  //sh 'which docker'  
  //sh 'docker build -t "tomcat:petclinic" .'
  //sh 'docker stop $(docker ps -a -q)'
 // sh 'docker run -d -p 8083:8080 -e TOMCAT_PASS="mypass" tomcat:petclinic'
}