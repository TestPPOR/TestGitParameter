pipeline {
    agent any
    parameter {
        password description: 'Password1', name: 'MYPASSWORD1'
        password description: 'Password2', name: 'MYPASSWORD2'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello'
            }
        }
    }
}