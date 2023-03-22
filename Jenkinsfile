pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f 01-primer-pipeline/Dockerfile -t miguels2401/homer_page:1.0.0-${BUILD_ID} 01-primer-pipeline"
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push miguels2401/homer_page:1.0.0-${BUILD_ID}"
                }
            }
        }
    }
}