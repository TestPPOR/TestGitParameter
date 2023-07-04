pipeline {
    agent any

    stages {
        stage('Delete workspace before build starts') {
            steps {
                echo 'Deleting workspace'
                deleteDir()
            }
        }
        stages {
            stage('Process start') {
                steps {
                    sh "echo GIT PARAMETER PROCESS SUCCESS"
                }
            }
        }
        stage('Ls work dir') {
        steps {
            sh '''
                ls -la                  
            '''
        }
        }
    }
}