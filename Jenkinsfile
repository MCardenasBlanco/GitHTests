pipeline{
    agent none
    stages{
        stage('MacOSX') {
            when { expression {false} }
            agent { label 'MacOSX' }
            steps { echo 'LINUX' }
        }
        stage('linux') {
            when { expression {true} }
            agent { label 'default' }
            steps { echo 'Running in the agent with the label default' }
        }
    }
}
