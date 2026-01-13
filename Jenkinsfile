pipeline {
    agent any
    stages 
    {
        stage('Checkout code') 
        {
            steps 
            {
                echo 'Pulling code from github'
                checkout scm
            }
        }
        
        stage('Build') 
        {
            steps 
            {
                echo 'Building the application'
                sh 'ls -l'
            }
        }
        
        stage('Test') 
        {
            steps 
            {
                echo 'Testing the application'
                sh 'bash test.sh'
            }
        }
        
        stage('Deploy') 
        {
            steps 
            {
                echo 'Deployiing the appication'
                sh 'echo  "Website CI pipeline executed successfully!"'
            }
        }

        stage('Post')
        {
            success
            {
                echo "CI pipeline Sucess"
            }
            failure
            {
                echo "CI pipeline Failure"
            }
        }
        
    }
}
