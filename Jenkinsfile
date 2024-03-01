pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/huuduy8203/jenkins-github.git'
            }
        }
        stage("Build Artifact") {
            buildArtifact()
        }
        stage("Push Artifact") {
            pushArtifact()
        }
        stage("Deploy Artifact") {
            deployArtifact()
        }
    }
}
