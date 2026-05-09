pipeline{
    agent {
        node{
            label 'roboshop'
        }
    }
    environment {
        course = "jenkins"
    }

    options {
        disableConcurrentBuilds()
        timeout(time: 30, unit: 'SECONDS')
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'vedavyas', description: 'Who to greet?')
        choice(name: 'ENV', choices: ['Dev', 'Staging', 'Prod'], description: 'Target environment')
        booleanParam(name: 'DEBUG', defaultValue: true, description: 'Enable debug logs')
    }

    stages{
        stage ('Build'){
            steps{
                script {
                    sh """
                        echo "this is build stage"
                        echo "learning $course"
                    """
                }          
            }
        }
        stage ('test'){
            steps{
                script {
                    sh """
                        echo "this is test stage"
                        echo "Hello ${params.PERSON} on ${params.ENV}!"
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
            echo "Hi vedavyas"
        }
        success {
            echo "pipeline success"
        }
        failure {
            echo "pipeline failure"
        }
        
    }
}


/* this is very basic level of pipeline where we use declarative + scripted pipeline, options, parameters, environments, agents, webhooks, post */