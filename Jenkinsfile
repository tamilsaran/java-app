node {
	stage('preparation') {
	    checkout scm
	}
	stage('build') {
        mvn -f java-sample-app/pom.xml clean install 
	}
}
