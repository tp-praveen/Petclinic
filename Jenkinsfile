node {
  stage 'Build-Master'  
  
	def proc = 'ls /badDir'.execute()
	proc.consumeProcessOutput(sout, serr)
	proc.waitForOrKill(1000)
	println "out> $sout err> $serr"

  //checkout scm
  //echo 'maven clean install skipping tests'
  //sh 'mvn clean install -DskipTests'
  //echo 'stopping docker container if running'
  //def tst = sh '$(docker ps | grep tomcat:petclinic | grep -o '^[0-9a-z]*')'  
  //echo 'docker id:'+$existing
  //if [ ! -z '''$existing''' ]; then  
  // sh 'docker stop $existing'
  //fi 
  //sh 'which docker'  
  //sh 'docker build -t "tomcat:petclinic" .'
  //sh 'docker stop $(docker ps -a -q)'
 // sh 'docker run -d -p 8083:8080 -e TOMCAT_PASS="mypass" tomcat:petclinic'
}