pipeline {
    agent any
    
    stages {
        stage('Verify Branch') {
            steps {
                echo "${GIT_BRANCH}"
            }
        }
        
        stage('Docker Build') {
            steps {
                powershell(script: 'docker images -a')
                pwsh(script: 'docker images -a')
                pwsh(script: """
                      cd azure-vote/
                      docker images -a
                      docker build -t jenkins-pipeline.
                      docker images -a
                      cd ..
                """)
            }
        }
        
        stage('Powershell script stage') {
            steps {
                powershell 'Write-Output "Hello power shell"'
            }
        }
    }
}