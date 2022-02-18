pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                pullRequest.review('REQUEST_CHANGES', 'Change is the essential process of all existence.')

                echo 'Hello World'
                
                
               /* for (reviewComment in pullRequest.reviewComments) {
                    echo "File: ${reviewComment.path}, Position: ${reviewComment.position}, Author: ${reviewComment.user}, Comment: ${reviewComment.body}"
                   }
                
                
                */
                
                
            }
        }
    }
    post {
        failure {
            script {
                // CHANGE_ID is set only for pull requests, so it is safe to access the pullRequest global variable
                if (env.CHANGE_ID) {
                    pullRequest.addLabel('Build Failed')
                    echo 'Build Failed'
                    
                }
                 echo 'Build out of IF '

            }
        }
    }
}
