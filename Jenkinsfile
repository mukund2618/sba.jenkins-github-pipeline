pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        powershell 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        powershell 'python test.py'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
