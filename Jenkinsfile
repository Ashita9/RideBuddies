pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('build'){
            steps {
                sh 'ls'
                dir('WebContent/'){
                    sh 'jar -cvf RideBuddies.war *'
                    sh 'docker build -t ashita9/ride:v1 -f Dockerfile .'
                    sh 'docker push ashita9/ride:v1'
                }
            }
        }
    }
}