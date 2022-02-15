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
                    patterns: [[pattern: '**/node_modules/**', type: 'EXCLUDE'],[pattern: '/src/sample/packages', type: 'EXCLUDE']])
        }
    }
}
