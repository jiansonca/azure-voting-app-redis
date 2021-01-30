pipeline {
    agent any
    
    stages {
        stage('Verify Branch') {
            steps {
                echo $GIT_BRANCH
            }
        }
        
        stage('Good bye') {
            steps {
                echo 'bye hello world.'
            }
        }
        
        stage('Powershell script stage') {
            steps {
                powershell 'Write-Output "Hello power shell"'
            }
        }
    }
}