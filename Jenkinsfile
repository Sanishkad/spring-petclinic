pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install'
            }
        }
        stage('Generate Code Coverage') {
            steps {
                echo 'Generating code coverage report...'
                sh 'mvn jacoco:prepare-agent jacoco:report'
            }
        }
    }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
            jacoco(execPattern: 'target/jacoco.exec')
        }
    }
}
