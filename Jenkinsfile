pipeline {
    agent any
    stages {
        stage('Build'){
            steps{
                echo "Build started and completed!"
            }
        }
        stage('Test'){
            steps{
                echo "Test started and completed!"
            }
        }
        stage('Deployment'){
            steps{
                retry(3){
                    sh 'command fails'
                }
                echo "Deployment started and completed!"
            }
        }
    }
}