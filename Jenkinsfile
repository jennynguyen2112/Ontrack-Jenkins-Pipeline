pipeline {
    agent any
    environment {
        DIRECTORY_PATH = 'C:/Users/phuon/Downloads/Trimester 2.2024/SIT753 Professional Practice in IT/Week 6'
        TESTING_ENVIRONMENT = 'Test_Env'
        PRODUCTION_ENVIRONMENT = 'Prod_env'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Initial build process using Maven'
            }
        }
        stage('Unit and Intergration Test') {
            steps {
                echo 'unit tests'
                echo "integration tests"
            }
            post {
                always {
                    emailext(
                        to: "huong.nguyenlinh96@gmail.com",
                        subject:"Unit and Intergration test email 2",
                        body: "Test Succeeded",
                        attachLog: true
                      )
                }

            }
        }
        stage('Code Analysis') {
            steps {
                echo 'perform code analysis'
            }
        }
         stage('Security Scan') {
            steps {
                echo 'conduct security scan'
            }
            post{
                always {
                    emailext(
                        to: "huong.nguyenlinh96@gmail.com",
                        subject:"Security Scan email 2",
                        body: "Scan Succeeded",
                        attachLog: true
                    )    
                }
   
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'deploy the application to staging environment!!'
            }
        }
        stage('Intergration test on Staging') {
            steps {
                echo 'run intergration test on staging'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production Environment '
            }
        }
    }
}
