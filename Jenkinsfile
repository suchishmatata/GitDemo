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
            bat """Del "${env.workspacePath}" -exclude ".git/**" """
           // Remove-Item c:\\tryremove\\* -exclude dontremove.txt
//             cleanWs(deleteDirs: true,
//                     disableDeferredWipeout: true,
//                     patterns: [
//                         [pattern: '.git/**', type: 'EXCLUDE'],
//                         [pattern: '/src/sample/node_modules/**', type: 'EXCLUDE'],
//                         [pattern: '//src//sample//packages/**', type: 'EXCLUDE']
//                     ])
        }
    }
}
