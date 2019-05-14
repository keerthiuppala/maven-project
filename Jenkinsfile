@Library('pipeline-library-demo')_

spipeline {
    agent any
	
	options {
    skipDefaultCheckout(true)
	}
	environment {
        branch = 'master'
		gitUrl = 'https://github.com/Nagagopi/maven-simple.git'
		gitCredentials = ' '
		buildTool = 'maven'
		mavenGoals = 'clean package'        
    }
    stages {
		stage('Checkout') {
			steps {
				scmFile()
			}
		}
		stage('Build') {
			steps {
				buildFile()
			}
		}
		

	}

}
