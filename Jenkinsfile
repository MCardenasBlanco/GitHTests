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
    println currentBuild.rawBuild.changeSets.size()
    //https://support.cloudbees.com/hc/en-us/articles/217630098-How-to-Access-Changelogs-in-a-Pipeline-Job
    //Test
}


