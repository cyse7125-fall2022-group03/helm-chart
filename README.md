# helm-chart

| Name                | NUID      | Email                          |
| ------------------- | --------- | ------------------------------ |
| Ketki Kule          | 001549838 | kule.k@northeastern.edu        |
| Sandeep Wagh        | 001839964 | wagh.sn@northeastern.edu       |
| Vignesh Gunasekaran | 001029530 | gunasekaran.v@northeastern.edu |

## Validate helm chart
cd app

```
helm lint . 
```

```
helm template .
```

Install helm chart 

move outside the helm chart directory 
 cd ../

```
helm install v1-app app
```


## File Structure

### Jenkinsfile 

Contains the git repo info 

### releaserc 

Used for semantic versioning


