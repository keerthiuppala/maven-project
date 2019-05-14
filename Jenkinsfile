@Library('pipeline-library-demo')_

pipeline {
    agent any
	
	options {
    skipDefaultCheckout(true)
	}
	environment {
        branch = 'master'
		gitUrl = 'https://github.com/Nagagopi/maven-simple.git'
		gitCredentials = ' '
		buildTool = 'maven_home'
		echo "${buildTool}"
		mavenGoals = 'clean package'        
    }
    stages {
		stage('Build') {
			steps {
				buildFile()
			}
		}
		

	}

}
