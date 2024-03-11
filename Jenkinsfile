pipeline {
    agent any

    triggers {
        cron('H/10 * * * 1')
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Generate Code Coverage Report') {
            steps {
                bat 'mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent package jacoco:report'
            }

            post {
                always {
                    jacoco(execPattern: 'target/**.exec')
                    publishHTML(target: [
                        allowMissing: false,
                        alwaysLinkToLastBuild: false,
                        keepAll: true,
                        reportDir: 'target/site/jacoco',
                        reportFiles: 'index.html',
                        reportName: 'Code Coverage Report'
                    ])
                }
            }
        }
    }
}
