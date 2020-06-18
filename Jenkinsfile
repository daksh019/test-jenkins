pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                script {
                    'ng lint'
                }
            }
        }
        stage('Test') {
            steps {
                script {
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
