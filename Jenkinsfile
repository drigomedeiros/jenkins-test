pipeline {

    agent any

    environment {
        COMMIT_SHA = "rodrigo"
    }

    stages {

        stage('Set commit'){
            steps {
                script {
                    if("${env.COMMIT_SHA}" != "") {
                        sh "echo ${env.COMMIT_SHA}"
                    }
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
