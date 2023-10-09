pipeline{
    agent{
        label "Agent"
    }
    // triggers{
    //     pollSCM('* * * * *')
    // }
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
                bat 'python test_calculator.py'
                //bat 'python -m pytest --verbose --junit-xml reports/unit_tests.xml'
            }
            post{
                always{
                    //junit allowEmptyResults: true, testResults: 'reports/unit_tests.xml'
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
        stage ("Test Report Generation")
        {
            steps{
                // bat 'java -Xms1300m -Xmx1300m -classpath "myClassPath;anotherone;anotherOne" -Xdebug "-Djava.compiler=NONE" "-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=5005"'
                // bat 'javac Palindrome.java'
                // bat 'java Palindrome'
                // bat 'javac PalindromeTest.java'
                // bat 'java PalindromeTest'
                
                bat 'python -m pytest --verbose --junit-xml reports/unit_tests.xml'
            }
            post{
                always{
                    junit allowEmptyResults: true, testResults: 'reports/unit_tests.xml'
                }
                success{
                    echo "========Calculator Test Cases executed successfully========"
                }
                failure{
                    echo "========Calculator Test Cases execution failed========"
                    echo "HI Hello"
                }
            }
        }
        // stage ("Email Notification")
        // {
        //     steps{
        //         // bat 'java -Xms1300m -Xmx1300m -classpath "myClassPath;anotherone;anotherOne" -Xdebug "-Djava.compiler=NONE" "-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=5005"'
        //         // bat 'javac Palindrome.java'
        //         // bat 'java Palindrome'
        //         // bat 'javac PalindromeTest.java'
        //         // bat 'java PalindromeTest'
        //         // bat 'python operations.py'
        //         // bat 'python unit-test.py'
        //         echo "Trying to send Email"
        //     }
        //     post{
        //         always{
        //             echo "========always========"
        //         }
        //         success{
        //            mail to : "gauravpandey17032002@gmail.com",
        //            subject : "Test Email",
        //            body : "Test"
        //         }
        //         failure{
        //             echo "========Calculator Test Cases execution failed========"
        //         }
        //     }
        // }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
            mail to : "gauravpandey17032002@gmail.com",
            subject : "Pipeline Completed",
            body : "Pipeline Completetd and test report generated"
        }
        failure{
            echo "========pipeline execution failed========"
            mail to : "gauravpandey17032002@gmail.com",
            subject : "Pipeline Failed",
            body : "Pipeline Failed"
        }
    }
}
