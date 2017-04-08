
//test -change Jenkinsfile
node {
try {
node() {
    sh "env"
   
    stage ('Build') {
    echo "Compile, run unit tests, publish to Nexus, publish coverage"
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GHMCB', url: 'https://github.com/MCardenasBlanco/GitHTests.git']]])//sh 'mvn clean install -U -Dmaven.test.skip=true'
    setBuildName("")
   }
    checkpoint 'Finished Build'
    
    if (release == "Yes") {
        echo "Release to Nexus"
        sh 'echo "$(git describe --tags `git rev-list --tags --max-count=1`)" >latestTag.properties'
        currentBuild.displayName = readFile 'latestTag.properties'
        setBuildName("RELEASE.")
        

        keepLog(true)
        currentBuild.keepLog(true)
   
}

}
    checkpoint 'Created Release'
   
    stage ('Deploy to CD') {
    node() {
       echo "Deployed to Nexus"
    }
    }
    checkpoint 'Deployed to CD'
   
    stage ('Deploy to DEV') {
    if (Dev == "Yes") {
        node() {
             echo "Deployed to Dev"
        }
    } else {
        echo ">>> Skipping stage DEV..."
    }
    }
    checkpoint 'Deployed to DEV'
   
stage ('Deploy to INT') {
if (INT == "Yes") {
     echo "Deployed to Int"
} else {
    echo ">>> Skipping stage INT..."
}
}
checkpoint 'Deployed to INT'
 
stage ('Deploy to QA') {
if (QA == "Yes") {
   echo "Deployed to QA"
} else {
    echo ">>> Skipping stage QA..."
}
}
checkpoint 'Deployed to QA'
 
stage ('Deploy to UAT') {
    if (UAT == "Yes") {
    echo "Deployed to UAT"
    } else {
        echo ">>> Skipping stage UAT..."
    }
    }
checkpoint 'Deployed to UAT'
 
stage ('Approve for production') {
if (release == "Yes" && QA == "Yes") {
     echo "Deployed to PRO"
}
}
} catch (e) {
    currentBuild.result = "FAILED"
    notifyFailed()
    throw e
  }
}
def setBuildName(append) {
    
    currentBuild.displayName = "${append}${env.BUILD_NUMBER}.Dummy"
}
