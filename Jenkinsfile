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
  
      post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
            mail to: 'team@example.com',
              subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
              body: "Something is wrong with ${env.BUILD_URL}"
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
