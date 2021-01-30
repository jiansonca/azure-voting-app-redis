pipeline {
    agent any
    
    stages {
        stage('Verify Branch') {
            steps {
                echo "${BRANCH_NAME}"
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