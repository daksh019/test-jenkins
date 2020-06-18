pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                script {
                    echo 'linting now'
                    'ng lint'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'testing now'
                    'ng test'
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
        failure {
            echo 'All steps pass!'
        }
        success {
            echo 'All steps fail!'
        }
    }
}
