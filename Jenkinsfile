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
                    # Commands to build the artifact should go here
                '''
                // buildArtifact() // Un-comment this line if buildArtifact is a defined method
            }
        }
        stage("Push Artifact") {
            steps {
                sh '''
                    echo "Push Artifact"
                    # Commands to push the artifact should go here
                '''
                // pushArtifact() // Un-comment this line if pushArtifact is a defined method
            }
        }
        stage("Deploy Artifact") {
            steps {
                sh '''
                    echo "Deploy Artifact"
                    # Commands to deploy the artifact should go here
                '''
                // deployArtifact() // Un-comment this line if deployArtifact is a defined method
            }
        }
    }
}
