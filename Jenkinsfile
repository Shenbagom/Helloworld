pipeline {

    agent {
        node {
            label 'master'
        }
    }

    options {
        buildDiscarder logRotator( 
                    daysToKeepStr: '16', 
                    numToKeepStr: '10'
            )
    }

    stages {
        
      stage("Env Variables"){
            steps{
                bat "set"                                                     
            }
      }

        stage('Analysis') {
            steps {
                
                echo 'Pulling...' + env.BRANCH_NAME
                checkout scm
                echo 'Pull Request..'+ env.CHANGE_ID
               
            }
            
            
            post {
        failure {
            script {
                // CHANGE_ID is set only for pull requests, so it is safe to access the pullRequest global variable
                if (env.CHANGE_ID) {
                    pullRequest.addLabel('Build Failed')
                }
            }
        }
    }
            
            
            
            
            
            
            
            
            
        }

     
       


    }   
}
