pipeline{
    agent {
        node {
            label 'agent-1'
        }
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
                echo 'building'
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