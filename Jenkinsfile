pipeline {
  agent any
    {
     stages{
       stage("test") {
            steps {
                script {
                    echo "Testing the application"
                    echo "Executing pipeline for branch $BRANCH_NAME"
                }
            }
        }
        stage("Build") {
            when{
                expression{
                    BRANCH_NAME == "main"
                }
            }
            steps {
                script {
                    echo "Building the application"
                }
            }
        }
        stage("Deploy") {
                when{
                expression{
                    BRANCH_NAME == "main"
                }
            }
            steps {
                script {
                     echo "Deploying the application"
                }
            }
        }
      
    }
}
}
