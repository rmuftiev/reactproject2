pipeline {

  agent any

  tools {nodejs "node"}

  stages {       

    stage('Install dependencies') {

      steps {
        sh 'npm install && npm run build'
      }
    }  

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
  }

    post {
            always {
                archiveArtifacts artifacts: 'build/**', onlyIfSuccessful: true
            }
        }

}



