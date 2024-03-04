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
                configFileProvider([configFile(fileId: '	00c3ceb0-126f-4ba3-82f8-b2593bd5068b', targetLocation: 'settings.xml')]) {
                    sh 'mvn deploy -DskipTests --settings settings.xml'
                }
            }
        }
    }
}

