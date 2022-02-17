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
        
        
      
        def scmVars = checkout scm
        def branchName = scmVars.GIT_BRANCH

         echo 'Pulling... ' + branchName
       


    }   
}
