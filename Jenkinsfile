
pipeline {
    environment{
        AGENT="test"
    }
    agent { label "$AGENT" } 
    stages {
        stage('Example Build') {
            
            steps {
                echo 'Hello, Maven'
                sh 'mvn --version'
            }
        }
        stage('Example Test') {
          
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
                echo AGENT
                echo "${AGENT}"
                echo "${env.AGENT}"
            }
        }
    }
}
