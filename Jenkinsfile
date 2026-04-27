pipeline {
    agent any

    tools {
        maven 'Maven'   // configure in Jenkins global tools
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/sriman0818/Jenkins-CI-CD.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
