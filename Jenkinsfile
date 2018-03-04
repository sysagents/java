pipeline {
    agent {
	label 'docker'
        
        }
    stages {
        stage('Build') {
            steps {
               echo 'This is a master pipeline.'
               echo 'This is a master and Webhook triggerd.'
        }
        when {
        branch 'dev'
               }

                }
    }
}


