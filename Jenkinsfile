pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'gcc hello.c -o hello'
            }
        }

        stage('Run') {
            steps {
                sh './hello'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
