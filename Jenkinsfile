pipeline {
    agent {
        docker {
            image 'maven:3.8.6-eclipse-temurin-8-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}