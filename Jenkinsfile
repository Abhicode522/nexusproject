pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo "mvn install"'
                sh 'mvn install'
            }
        }
        stage('Build the docker image') {
            steps {
                sh 'echo "docker build"'
                sh 'docker build -t dockeabhi095/nexusimage:v1 . && docker images'
                sh 'docker images'
            }
        }
        stage('push the docker image') {
            steps {
               sh 'echo "docker push"'
               sh 'docker push dockeabhi095/nexusimage:v1'
               sh 'docker rmi dockeabhi095/nexusimage:v1'
               sh 'docker images' 
            }
        }
    }
}
