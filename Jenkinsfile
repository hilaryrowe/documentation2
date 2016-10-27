#!groovy

// Jenkins Job Configuration
// Search http://jenkins.int.sightmachine.com/job/fe-react-pipeline/pipeline-syntax/html for "properties"

// Jenkins Pipeline
timeout(10) {
    node('docker') {
        timestamps {
	    stage("Build + Test") {
	        checkout scm
                gitDescribe = sh "git describe"
	        wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'XTerm']) {
		    sh "./jenkins/build.sh"
	        }
	    }
	     
	    stage("Archive") {
	        archiveArtifacts 'artifacts/**.tar.gz'

                sh "./jenkins/archive_to_s3.sh"

	        sh "./jenkins/clean.sh"
	   }
        }
    }
}
