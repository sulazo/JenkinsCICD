
pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage('Fetch Code') {
            steps {
                 //git 'git@github.com:sulazo/JenkinsCICD.git
                 git branch: 'main', url: 'https://github.com/sulazo/JenkinsCICD.git'
            }
        }
        stage('Maven Build') {
            steps {
                sh 'mvn install -DskipTests'
            }
        }
        post{
            success{
                echo "Now archiving"
            }
        }


        stage("Unit test"){
            sh "mvn test"
        }
    }
}