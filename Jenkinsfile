pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: '12345', url: 'https://github.com/liqb-pro/liquibase.properties.git'
            }
        }

        stage('Run Liquibase') {
            steps {
                sh "liquibase --changeLogFile=changelog.xml update"
            }
        }
    }
}
