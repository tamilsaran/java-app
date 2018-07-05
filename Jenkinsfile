node {
	stage('preparation') {
	    checkout scm
	}
	stage('build') {
        /var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven/bin/mvn -f java-sample-app/pom.xml clean install 
	}
}
