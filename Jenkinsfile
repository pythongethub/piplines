pipeline {
    agent any
    tools {
        maven 'maven 3.8.8'
    }
    stages {
        stage ('version'){
            steps{
                sh 'mvn --version'
            }
        }
        stage('jdk version'){
            tools{
                jdk 'jdk17'
            }
            steps{
                sh 'jdk --version'
            }
        }
    }
}
