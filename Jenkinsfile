pipeline {

    agent any

    environment {
        COMMIT_SHA = ""
    }

    stages {

        parallel {

            stage('Set commit'){
                steps {
                    script {
                        if(env.COMMIT_SHA != null) {
                            sh "git reset --hard ${env.COMMIT_SHA}"
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

        parallel {

            stage('Set commit'){
                steps {
                    script {
                        if(env.COMMIT_SHA != null) {
                            sh "git reset --hard ${env.COMMIT_SHA}"
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
}
