# helm-chart

| Name                | NUID      | Email                          |
| ------------------- | --------- | ------------------------------ |
| Ketki Kule          | 001549838 | kule.k@northeastern.edu        |
| Sandeep Wagh        | 001839964 | wagh.sn@northeastern.edu       |
| Vignesh Gunasekaran | 001029530 | gunasekaran.v@northeastern.edu |


Final documentation of API call 
```
https://documenter.getpostman.com/view/18309852/2s8YK9KR11
```

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

Pulls the latest release

### releaserc 

Used for semantic versioning

### app

Contains helm chart


