pipeline {
    agent {
        node {
            label 'Agent1'
        }
    }
    
    stages {
        stage('testing') { 
            steps {
                 script{
                    sh " " "
                    echo 'Hello World'

                    " " "

                } 
            }
        }
        stage('build') { 
            steps {
                script{
                    sh " " "
                    echo 'Hello World' 

                    " " "

                }
                
            }
        }
        stage('deploy') { 
            steps {
                 script{
                    sh " " "
                    echo 'Hello World' 
                    
                    " " "

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
    }
}