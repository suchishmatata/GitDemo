pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
                echo 'deployed'
            }
        }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
