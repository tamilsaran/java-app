pipeline {
	agent { label 'cent'}
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
			    sh 'rm -rf /chef-repo/cookbooks/tomcat/files*'
			    sh 'mv /home/zippyops/jenkins/workspace/project/java-sample-app/target/java-sample-app-1.0.0.war /chef-repo/cookbooks/tomcat/files'
		}
	}
        }
		}	
