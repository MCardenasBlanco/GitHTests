#!groovy

stage 'Dev'
node () {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
              doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
              userRemoteConfigs: [[url: 'https://github.com/MCardenasBlanco/pipeline-as-code-demo']]])
    sh 'ls -lrt'
    sh 'echo $env.BUILD_NUMBER'
}
