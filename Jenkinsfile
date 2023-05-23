
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
               post{
            success{
                echo "Now archiving"
            }
        }
        }
        stage("email")
        steps{
            mail bcc: '', body: '''Hello ,
            Email notice from jenkins ''', cc: '', from: '', replyTo: '',
            subject: 'Email notification', to: 'sholashokunbi2015@gmail.com'
        }
     


        // stage("Unit test"){
        //     steps{
        //     sh "mvn test"
        //     }
        // }
    }
}