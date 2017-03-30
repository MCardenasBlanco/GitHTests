#!groovy

//Comments included-for replication purposes
stage 'Dev'
node () {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
              doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
              userRemoteConfigs: [[url: 'https://github.com/MCardenasBlanco/pipeline-as-code-demo']]])
    sh 'ls -lrt'
    println "Build: ${env.BUILD_NUMBER}"
    println "Build $env.BUILD_NUMBER"
    println myTest()
}

@NonCps def myTest(){
 return Jenkins.instance.getAllItems(Job).size().toString()   
}
