pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        powershell "py -m pip install -r requirements.txt"
	powershell "py web.py"
      }
    }
    stage('test') {
      steps {
        powershell "py test.py"
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
