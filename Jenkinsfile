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
        
      

        stage('Analysis') {
            steps {
                
                echo 'Pulling...' + env.BRANCH_NAME
                checkout scm
            }
        }

     
       


    }   
}
