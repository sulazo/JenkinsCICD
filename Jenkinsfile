
pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage('Fetch Code') {
            steps {
                // git 'https://github.com/sulazo/JenkinsCICD.git'
                  git branch: 'feature1', url: 'https://github.com/sulazo/smanstudios-complete-CICD.git'
            }
        }
        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}