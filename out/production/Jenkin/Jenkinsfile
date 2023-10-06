pipeline{
    agent{
        label "Agent"
    }
    stages{
        stage("Hello"){
            steps{
                echo "========executing Hello Stage========"
                bat 'python --version'
                bat 'python myfile.py'
                
                //bat 'python main.py'
                
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
        stage ("Junit Test Run")
        {
            steps{
                bat 'javac Palindrome.java'
                bat 'java Palindrome'
                bat 'javac PalindromeTest.java'
                bat 'java PalindromeTest'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Palindrome executed successfully========"
                }
                failure{
                    echo "========Palindrome execution failed========"
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
