pipeline {
    agent  {
        label 'AGENT-1'
    }
    environment { 
        COURSE = 'JENKINS'
    }
    
    // Build
    stages {  // goovy based 
        stage('Build') {
            steps {
                script{
                  sh """

                  echo 'hey Building..' 
                  env

                """ 
                }
            }
        }
        stage('Test') {
            steps {
                script{
                  echo 'nice Testing..' 
                  env 
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script{
                    echo 'Deploying..'
                }
            }
        }
        
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'Hello Success'
        }
        failure { 
            echo 'Hello Failure'
        }
    }
}