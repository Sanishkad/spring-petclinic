pipeline {
    agent any
    
    triggers {
        cron('H/10 * * * 1')
    }

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/SanishKad/spring-petclinic.git'
                script {
                    sh 'mvn clean install'
                }
            }
        }
        stage('Code Coverage') {
            steps {
                script {
                    sh 'mvn jacoco:prepare-agent test jacoco:report'
                }
                junit '**/target/surefire-reports/TEST-*.xml'
                jacoco(execPattern: '**/target/jacoco.exec')
            }
        }
    }

    post {
        always {
            jacoco(execPattern: '**/target/jacoco.exec')
            jacoco(execPattern: '**/target/jacoco-it.exec')
            jacoco(execPattern: '**/target/coverage-reports/jacoco-merged.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.ec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
            jacoco(execPattern: '**/target/jacoco/*.exec')
        }
    }
}
