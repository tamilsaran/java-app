pipeline {
	agent {label 'cent'}
    stages {
        stage ('checkout') {
            steps {
		checkout scm
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn -f java-sample-app/pom.xml clean install' 
            }
        }
	    stage ('move') {
		    steps {
			    sh "sudo mv /root/home/zippyops/jenkins/workspace/projects/java-sample-app/target/java-sample-app-1.0.0.war /root/etc/puppetlabs/code/environments/production/modules/cat/files"     
		    }
	}
        }
		}	
