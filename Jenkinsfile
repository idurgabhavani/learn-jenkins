pipeline{
    agent {
        node {
            label 'agent-1'
        }
    }

    environment {
        GREETING = 'hello jenkins'
    }
    options {
        timeout(time: 1, unit: 'SECONDS')
        disableConcurrentBuild()  // this will stops if again and again building the same pipelins
    }

    stages{
        stage('Build') {
            steps {
                echo 'building'
            }

        } 
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                steps {
                    sh """

                    echo " hello this is shell script"
                    echo "$GREETING"
                    sleep 10

                    """


                }
                
            }
        }
        
    }
}

// post build

post {
    always {
        echo 'it will always say hello again'
    }
    failure {
        echo ' it will run when pipline is failed, used generally to send alrets '
    }
    success{
        echo ' ur pipe is success'
    }
}