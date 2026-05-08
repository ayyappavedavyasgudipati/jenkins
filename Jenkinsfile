pipeline{
    agent {
        node{
            label 'roboshop'
        }
    }
    stages{
        stage ('Build'){
            steps{
                script {
                    sh """
                        echo "this is build stage"
                    """
                }          
            }
        }
        stage ('test'){
            steps{
                script {
                    sh """
                        echo "this is test stage"
                    """
                }          
            }
        }
        stage ('deploy'){
            steps{
                script {
                    sh """
                        echo "this is deploy stage"
                    """
                }          
            }
        }
    }

    post {
        always {
            "Hi vedavyas"
        }
    }
}


/* declarative + scripted pipeline */