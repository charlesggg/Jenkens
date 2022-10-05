pipeline {
    agent any
    stages {
        stage('build') {        
                steps {
                    withMaven(maven: 'mvn') {
                        sh 'mvn --version'
                    }
                }
            
        }
    }
}
