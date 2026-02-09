pipeline {
    agent  {
        label 'AGENT-1'
    }
    environment { 
        COURSE = 'JENKINS'
    }
    options {
        timeout(time: 10, unit: 'SECONDS')
        disableConcurrentBuilds() 
    }
    
    // Build
    stages {  // goovy based 
        stage('Build') {
            steps {
                script{
                  sh """

                  echo 'hey Building..' 
                  sleep 10
                  env

                """ 
                }
            }
        }
        stage('Test') {
            steps {
                script{
                  echo 'nice Testing..' 
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