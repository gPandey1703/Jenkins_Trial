pipeline{
    agent{
        label "Agent"
    }
    stages{
        stage("Hello"){
            steps{
                echo "========executing Hello Stage========"
                sh 'python3 --version'
                sh 'python3 myfile.py'
                sh 'python3 main.py'
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
