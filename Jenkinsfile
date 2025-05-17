pipeline {
    agent {label 'AGENT-1'} 
    environment{
        PROJECT='expense'
        COMPONENT='backend'
    }
    options{
        disableConcurrentBuilds()
    }
        stages{
            stage("Build"){
                steps{
                    script{
                        sh """
                        echo "Hello, this is Build "
                        echo "project is: $PROJECT"
                        """
                    }
                }
            }
            stage("Test"){
                steps{
                    script{
                        sh """
                        echo "Hello, this is Test"
                        """
                    }
                }
            }
            stage("Deploy"){
                steps{
                    script{
                        sh """
                        echo "Hello, this is Deploy"
                        """
                    }
                }
            }
        }
        post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        failure { 
            echo 'I will run when pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }
}