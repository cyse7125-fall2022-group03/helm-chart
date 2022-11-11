# helm-chart

helm lint .

added symantic release


```
node
{

    stage('Clone repository') {
        git branch: 'main', credentialsId: 'jenkins-key-1', url: 'https://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@github.com/cyse7125-fall2022-group03/helm-chart.git'
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
```