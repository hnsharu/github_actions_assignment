pipeline {
    agent any

    stages {
        stage('Buildd') {
            steps {
                sh 'pip install -r requirements.txt'
                sh 'python src/calculate_area.py'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest --cov=./ --cov-report=xml'
            }
        }
        
    }
}
