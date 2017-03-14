#!groovy

stage 'Dev'
node () {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
              doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
              userRemoteConfigs: [[url: 'https://github.com/MCardenasBlanco/pipeline-as-code-demo']]])
    mvn 'clean package'
    dir('target') {stash name: 'war', includes: 'x.war'}
}
