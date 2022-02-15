pipeline {
    agent any
    stages 
    {
        stage('deploy') 
        {
            steps             
            {
                echo 'deployed'
            }
        }
//         stage('clean')
//         {
//             steps
//             {
//                 script
//                 {
// //                     def powerShellCommand = '.\\power.ps1'
// //                     def shellCommand = "powershell.exe -ExecutionPolicy Bypass -NoLogo -NonInteractive -NoProfile -Command \"${powerShellCommand}\""
// //                     def process = shellCommand.execute()
//                     bat """Del "${env.WORKSPACE}\\*" -exclude ".git/**" -Confirm:\$false -Force"""
//                 }
//             }
//         }
    }
    post
    {
        always{
//             bat """Del "${env.WORKSPACE}\\*" -exclude ".git/**" -Confirm:\$false -Force"""
           // Remove-Item c:\\tryremove\\* -exclude dontremove.txt
            cleanWs(
                    patterns: [
//                         [pattern: '.git/**', type: 'EXCLUDE'],
                        [pattern: 'src/sample/packages/**', type: 'EXCLUDE'],
                        [pattern: 'src/sample/node_modules/**', type: 'EXCLUDE']
//                         [pattern: '${env.WORKSPACE}\\src\\sample\\node_modules\\**', type: 'EXCLUDE'],
//                         [pattern: '${env.WORKSPACE}\\src\\sample\\packages\\**', type: 'EXCLUDE']
                    ])
            
        }
    }
}
