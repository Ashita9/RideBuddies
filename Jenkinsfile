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
                    sh 'docker build -t Ashita9/ride:v1 -f Dockerfile .'
                    sh 'docker push Ashita9/ride:v1'
                }
            }
        }
    }
}