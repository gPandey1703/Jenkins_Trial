pipeline{
    agent{
        label "Agent"
    }
    stages{
        stage("Hello"){
            steps{
                echo "========executing Hello Stage========"
                sh 'python myfile.py'
                sh 'python main.py'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Hello executed successfully========"
                }
                failure{
                    echo "========Hello execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
