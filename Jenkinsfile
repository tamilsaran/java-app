node {
	stage('preparation') {
	    checkout scm
	}
	stage('build') {
        mvn -f clean install 
	}
}
