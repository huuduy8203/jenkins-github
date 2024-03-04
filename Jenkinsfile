pipeline {
    agent any

    tools {
        // Use the name you've given your Maven installation
        maven 'Maven3' 
    }

    environment {
        // Define environment variables if needed
        NEXUS_CREDENTIALS = credentials('nexus')
    }

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

        stage("Push Artifact to Nexus") {
            steps {
                script {
                    // Assuming you're using Maven and the maven deploy command.
                    sh 'mvn deploy -DskipTests --settings /Users/nguyenhuuduy/Desktop/"My Mac"/Workspace/nexus/nexus-3.65.0-02/system/settings.xml'
                }
            }
        }
    }
}

