pipeline{
    agent any
    throttle(['test_2']) {
    node() {
        sh "sleep 500"
        echo "Done"
    }
}
    stages{
       
        stage('MacOSX') {
            steps{ echo 'test' }
        }
       
        stage('linux') {
            steps { 
                echo 'test'
                echo 'changes for new PR'  
            }
        }
        
    }
}
