pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
                echo 'deployed'
            }
        }
    }
    post
    {
        always{
            cleanWs(deleteDirs: true,
                    disableDeferredWipeout: true,
                    patterns: [[pattern: '.git', type: 'EXCLUDE']])
        }
    }
}
