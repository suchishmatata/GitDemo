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
//             bat """Del "${env.WORKSPACE}\\*" -exclude ".git/**" -Confirm:\$false -Force"""
           // Remove-Item c:\\tryremove\\* -exclude dontremove.txt
            cleanWs(deleteDirs: true,
                    disableDeferredWipeout: true,
                    patterns: [
                        [pattern: '.git/**', type: 'EXCLUDE'],
                        [pattern: '${env.WORKSPACE}\\src\\sample\\node_modules\\**', type: 'EXCLUDE'],
                        [pattern: '${env.WORKSPACE}\\src\\sample\\packages\\**', type: 'EXCLUDE']
                    ])
        }
    }
}
