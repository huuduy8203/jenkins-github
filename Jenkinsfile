pipeline {
    agent any

    tools {
        maven 'Maven3' 
    }

    environment {
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
                sh 'mvn clean package -DskipTests'
            }
        }
        stage("Push Artifact to Nexus") {
            steps {
                configFileProvider([configFile(fileId: '00c3ceb0-126f-4ba3-82f8-b2593bd5068b', targetLocation: 'settings.xml')]) {
                    sh 'mvn deploy -DskipTests --settings settings.xml'
                }
            }
        }
        stage("Deploy Artifact") {
            steps {
                // Replace the echo command with actual deployment commands
                echo 'Replace this echo command with actual deployment commands'
            }
        }
    }
}
