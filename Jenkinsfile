pipeline {
    agent any
    stages {
        stage('Build'){
            steps{
                echo "Using Apache Maven to automate build process"
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Using Selenium to automate testing process"
            }
            post
            {
                success{
                    emailext subject: "Unit and Integration Test Status, 6.1C",
                             body: "Unit and Integration Tests were successful",
                             to: "winnewissercedric@gmail.com"
                }            
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Using Coverity to automate code analysis"
            }
        }
        stage('Security Scan'){
            steps{
                echo "Using Nessus to automate security scanning"
            }
            post
            {
                success{
                    emailext subject: "Unit and Integration Test Status, 6.1C",
                             body: "Unit and Integration Tests were successful",
                             to: "winnewissercedric@gmail.com"
                }
            }            
        }
        stage('Deploy to Staging'){
            steps{
                echo "Deploying to AWS EC2 staging server"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Running integration tests on staging environment in AWS EC2"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploying application to production server, AWS EC2 instance"
            }
        }
    }
}
