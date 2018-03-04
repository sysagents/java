pipeline {
    agent {
	label 'docker'
        
        }
    stages {
        stage('Build') {
        when {
        branch 'development'
		}
	steps {
	sh 'git remote add origin git@github.com:sysagents/java.git'
        echo "Stashing Any Local Changes"
        sh 'git stash'
        echo "Checking Out Development Branch"
        sh 'git checkout development'
        echo 'Checking Out Master Branch'
        sh 'git pull origin'
        sh 'git checkout master'
        echo 'Merging Development into Master Branch'
        sh 'git merge development'
        echo 'Pushing to Origin Master'
        sh 'git push origin master'
      }
      }
    }  
}
