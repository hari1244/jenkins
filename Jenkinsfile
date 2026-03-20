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
        disableConcurrentBuilds()
        parameters {
            string(name: 'name', defaultValue: 'Jenkins', description: 'Enter your name')
            booleanParam(name: 'isTrue', defaultValue: true, description: 'This is a boolean parameter')
            choice(name: 'choice', choices: ['option1', 'option2', 'option3'], description: 'This is a choice parameter')
        }
    }
    
    stages {
        stage('testing') { 
            steps {
                 script{
                     sh  """
                    echo 'Hello World'
                    echo ${course}
                    env
                    sleep 10
                    echo " Hello ${params.name}"    
                    echo "Boolean parameter value: ${params.isTrue}"
                    echo "Choice parameter value: ${params.choice}"     
                

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