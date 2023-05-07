
pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage('Fetch Code') {
            steps {
                git 'https://github.com/sulazo/JenkinsCICD.git'
            }
        }
        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
