pipeline {
    agent {
        node {
            label 'Agent1'
        }
    }
    environment {
        course = 'Jenkins'
    }
    options {
        timeout(time: 10, unit: 'MINUTES')
    }
    
    stages {
        stage('testing') { 
            steps {
                 script{
                     sh  """
                    echo 'Hello World'
                    echo ${course}
                    env
                    #sleep 10

                    """

                } 
            }
        }
        stage('build') { 
            steps {
                script{
                     sh  """
                    echo 'Hello World'

                    """

                }
                
            }
        }
        stage('deploy') { 
            steps {
                 script{
                    sh  """
                    echo 'Hello World'

                    """

                }
            }
        }
    }
    post {
        always {
            echo 'This will always run'
            cleanWs()
        }
        success {
            echo 'This will run only if the build is successful'
        }
        failure {
            echo 'This will run only if the build fails'
        }
        aborted {
            echo 'This will run only if the build is aborted'
        }
    }
}