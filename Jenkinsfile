@Library('shared-lib') _

pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                script {
                    frontend.checkoutgit('https://github.com/Dev0046/frontend.git', 'main')
                }
            }
        }
    
        stage('Sonarqube') {
            steps {
                script {
                    frontend.callSonarqube()
                }
            }
        }
        
        stage('License') {
            steps {
                script {
                    frontend.License()
                }
            }
        }
        
        stage('CredScanning') {
            steps {
                script {
                    frontend.CredScanning()
                }
            }
        }
    }
}
