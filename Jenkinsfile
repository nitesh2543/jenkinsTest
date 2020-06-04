pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
               withMaven(maven: 'maven_3_5_1'){
               bat 'mvn clean compile'
               }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'maven_3_5_1'){
                    bat 'mvn test'
                }
            }
        }
        stage('Deployment Stage (WAR)') {
            steps {
                withMaven(maven: 'maven_3_5_1'){
                    bat 'mvn deploy'
                }
            }
        }
    }
}
