pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                'ng lint'
            }
        }
        stage('Test') {
            steps {
                'ng test'
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
