pipeline{
    agent any
    
    stages{
       throttle(['test_2']) {
    node() {
        sh "sleep 500"
        echo "Done"
    }
}
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
