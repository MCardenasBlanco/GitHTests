pipeline{
    agent none
    stages{
        stage('linux') {
            when { expression {false} }
            agent { label 'default' }
            steps { echo 'LINUX' }
        }
    }
}
