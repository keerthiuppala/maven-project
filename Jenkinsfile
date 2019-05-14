@Library('pipeline-library-demo')_

pipeline {
    agent any
	
	options {
    skipDefaultCheckout(true)
	}
	environment {
        branch = 'master'
		gitUrl = 'https://github.com/Nagagopi/maven-simple.git'
		gitCredentials = 'Nagagopi:horntail23'
		buildTool = 'maven_home'
		mavenGoals = 'clean package'
		artifactoryTool = 'artifactoryserver'
		uploadArtifacts = '*Maven*.war'
		uploadRepository = 'samplerepo/'
    }
    stages {
	    
	    stage('Checkout') {
			steps {
				scmFile(branch,gitUrl)
			}
		}
	    stage('Build') {
			steps {
				buildFile(buildTool)
			}
		}
	    stage('Upload Artifacts') {
			steps {
				uploadArtifactory(artifactoryTool)
			}
		}

	}

}
