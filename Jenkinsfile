pipeline {

    agent any

    environment {
        COMMIT_SHA = ""
    }

    stages {

        stage('Set commit'){
            steps {
                script {

                    sh "echo ${COMMIT_SHA}"

                }
            }
        }

        stage('Echo README') {
            steps {
                sh "cat README.md"
            }
        }

    }
}
