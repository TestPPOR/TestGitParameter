pipeline {
    agent any

    stages {
        stage('EnvironmentInjector') {
            steps {
                sh 'env | sort'
            }
        }
    }
}