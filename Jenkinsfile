pipeline {
    agent any
    stages {
        stage ('SBA - Build') {
		steps {
			//powershell "py -m ensurepip"
			//powershell "py -m pip install Flask"
			sh "py -m pip install -r requirements.txt"
			//powershell "py web.py"
		}
    }
}
}
