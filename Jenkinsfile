pipeline{
    agent none
    stages{
        stage('linux') {
            when { expression {false} }
            agent { label 'default' }
            steps { echo 'LINUX' }
        }
        stage('other') {
            when { expression {true} }
            agent { label 'default' }
            steps { echo 'Running in the agent with the label default' }
        }
    }
}
