pipeline {
    agent any

    stages {
        stage('Run tests') {
            steps {
                sh '''
                #!/bin/bash
                source /opt/venv/bin/activate
                python3 test_calculs.py
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline terminé avec succès !'
        }
        failure {
            echo 'Pipeline échoué !'
        }
    }
}

