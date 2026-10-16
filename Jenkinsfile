pipeline {
    agent any
stages {
    stage('Checkout') {
        steps {
            echo 'Getting project code'
            checkout scm
        }
    }

    stage('Test') {
        steps {
            echo 'Running Python tests'
            bat 'python --version'
            bat 'python -m unittest discover -s . -p "test_*.py" -v'
            }
        }
}
    post {
    success {
        echo 'CI Pipeline Successful!'
    }
    failure {
        echo 'CI Pipeline Failed!'
        }
    }
}
