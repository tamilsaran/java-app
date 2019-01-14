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
			    sh 'rm -rf /chef-repo/cookbooks/tomcat/files/*'
			    sh 'mv /home/zippyops/jenkins/workspace/upstream/java-sample-app/target/java-sample-app-1.0.0.war /home/zippyops/chef-repo/cookbooks/tomcat/files/'
		}
	}
        }
		}	
