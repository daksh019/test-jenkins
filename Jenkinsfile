pipeline {
 agent any
 stages {
        stage('Build') {
            steps {
              sh './scripts/installations.sh'
            }
        }
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
