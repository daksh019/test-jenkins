pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                sh 'ng lint'
            }
        }
        stage('Test') {
            steps {
                sh 'ng test'
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
