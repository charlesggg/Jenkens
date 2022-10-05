pipeline {
  agent any
  tools {
    maven 'mvn'
  }
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
