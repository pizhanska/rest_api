pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps{
                bat 'mvn -Dtest=TestClientMethods test'  
                publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'target/surefire-reports/html', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
            }  
             
        }
    }
}
