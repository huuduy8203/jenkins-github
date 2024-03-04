pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/huuduy8203/jenkins-github.git'
            }
        }
        stage("Build Artifact") {
            steps {
                sh '''
                    echo "Build Artifact"
                '''
            }
        }
        stage("Push Artifact") {
            steps {
                sh '''
                    echo "Push Artifact"
                '''
            }
        }
        stage("Deploy Artifact") {
            steps {
                sh '''
                    echo "Deploy Artifact"
                '''
            }
        }
    }
}
