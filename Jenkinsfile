pipeline {
    agent any
    stages {
        stage('build') {
            withMaven(maven: 'mvn') {
                steps {
                    sh 'mvn --version'
                }
            }
        }
    }
}
