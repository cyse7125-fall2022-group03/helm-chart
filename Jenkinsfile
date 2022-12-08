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

    stage ('Deploy') {
        sh"""
        export AWS_ACCESS_KEY_ID=${env.AWS_ACCESS_KEY_ID}
        export AWS_SECRET_ACCESS_KEY=${env.AWS_SECRET_ACCESS_KEY}
        export AWS_DEFAULT_REGION=${env.AWS_DEFAULT_REGION}
        export KOPS_STATE_STORE=${env.KOPS_STATE_STORE}
        kops export kubecfg ${env.CLUSTER_NAME} --state ${env.KOPS_STATE_STORE}
        helm upgrade --install --wait --set configmap.dbHost=${env.RDS_URL},flyway.url=${env.FLYWAY_URL} app ./app
        """    
    }
}