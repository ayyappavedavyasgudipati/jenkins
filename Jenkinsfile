pipeline{
    agent any
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
}


/* declarative + scripted pipeline */