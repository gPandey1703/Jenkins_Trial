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
        // stage ("Running Calculator File")
        // {
        //     steps{
        //         // bat 'java -Xms1300m -Xmx1300m -classpath "myClassPath;anotherone;anotherOne" -Xdebug "-Djava.compiler=NONE" "-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=5005"'
        //         // bat 'javac Palindrome.java'
        //         // bat 'java Palindrome'
        //         // bat 'javac PalindromeTest.java'
        //         // bat 'java PalindromeTest'
        //         bat 'python calc.py'
        //     }
        //     post{
        //         always{
        //             echo "========always========"
        //         }
        //         success{
        //             echo "========Calculator executed successfully========"
        //         }
        //         failure{
        //             echo "========Calculator execution failed========"
        //         }
        //     }
        // } 
        stage ("Running Operations and test file")
        {
            steps{
                // bat 'java -Xms1300m -Xmx1300m -classpath "myClassPath;anotherone;anotherOne" -Xdebug "-Djava.compiler=NONE" "-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=5005"'
                // bat 'javac Palindrome.java'
                // bat 'java Palindrome'
                // bat 'javac PalindromeTest.java'
                // bat 'java PalindromeTest'
                bat 'python operations.py'
                bat 'python unit-test.py'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Calculator Test Cases executed successfully========"
                }
                failure{
                    echo "========Calculator Test Cases execution failed========"
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
