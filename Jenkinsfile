node
{

    stage('Clone repository') {
        git branch: 'main', credentialsId: '${env.JENKINS_CRED_ID}', url: 'https://${env.TOKEN_GITHUB}@github.com/cyse7125-fall2022-group03/helm-chart.git'
    }
    
    

    stage('release')
    {
        sh "npm install @semantic-release/git -D"
        sh "npm install semantic-release-helm -D"
        sh "npm install @semantic-release/exec -D"
        sh  "npm install semantic-release-yaml -D"
        sh  "npx semantic-release"
        
    } 
}