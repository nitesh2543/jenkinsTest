pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
               echo "hello"
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'maven_3_5_1'){
                    bat 'mvn test'
                }
            }
        }
        stage('my test') {
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
