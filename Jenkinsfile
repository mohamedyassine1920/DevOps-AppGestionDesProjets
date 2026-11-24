pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                dir('backend') {
                    sh 'mvn compile'
                }
            }
        }
    }

    post {
        success { echo 'Compilation réussie : SUCCESS' }
        failure { echo 'Échec de la compilation' }
    }
}
