pipeline {

    agent any

    environment {
        COMMIT_SHA = ""
    }

    stages {

        stage('Set commit'){
            steps {
                script {
                    if($(COMMIT_SHA) != ""){
                        sh "git reset --hard $(COMMIT_SHA)"
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
