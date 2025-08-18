@Library('shared') _

def configMap = [
    application: "asus", // we are migrating monolithic to Microservice
    component: "mongodb"
]
env

// this is .groovy file name and function inside it
//if not master then trigger pipeline
if (!env.BRANCH_NAME.equalsIgnoreCase('master')){
    pipelineDecision.decidePipeline(configMap)
}
else{
    echo "master PROD deployment should happen through CR"
}
