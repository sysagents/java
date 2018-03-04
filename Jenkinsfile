pipeline {
    agent {
	label 'docker'
        
        }
    stages {
        stage('Build') {
        when {
        branch 'development'
	 steps {
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
       # echo 'Tagging the Release'
       # sh "git tag rectangle-${env.MAJOR_VERSION}.${env.BUILD_NUMBER}"
       # sh "git push origin rectangle-${env.MAJOR_VERSION}.${env.BUILD_NUMBER}"
      }
               }

                }
    }
}


