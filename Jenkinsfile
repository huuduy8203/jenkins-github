pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/huuduy8203/jenkins-github.git'
            }
        }
        stage("Build Artifact") {
            sh """
                echo "Build Artifact"
            """
            // buildArtifact()
        }
        stage("Push Artifact") {
            sh """
                echo "Build Artifact"
            """
            // pushArtifact()
        }
        stage("Deploy Artifact") {
            sh """
                echo "Build Artifact"
            """
            // deployArtifact()
        }
    }
}
