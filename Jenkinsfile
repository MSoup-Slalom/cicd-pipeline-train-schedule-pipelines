pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'gradle build' 
            }
        }
    }
    stages {
        stage('Deploy') {
            steps {
                sh 'zip dist/trainSchedule.zip ' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}

