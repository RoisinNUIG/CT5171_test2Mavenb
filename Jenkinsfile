pipeline {
    agent any

    stages {

        stage ('GetProject') {
            steps{
                git branch:'master', url: 'https://github.com/RoisinNUIG/CT5171_test2Mavenb.git'
            }
        }
        stage ('Build') {
            steps{
                sh "mvn clean:clean"
                sh 'mvn dependency:copy-dependencies'
                sh 'mvn compiler:compile'
            }
        }

                stage('Exec') {
                    steps{
                        sh 'mvn exec:java'
                    }
                }
            }
        }