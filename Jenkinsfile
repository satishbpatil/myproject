pipeline{
    agent any
    tools{
        maven 'M3'
    }
    stages{
        stage('checkout'){
            steps{
                git  'https://github.com/satishbpatil/myproject.git'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}