pipeline{
    agent any
    
    stages{
      
        stage('MacOSX') {
            
            steps{ echo 'test' 
                  throttle(['test_2']) {
    node('master') {
        sh "sleep 500"
        echo "Done"
    }
                 }
            
}
        }
       
        stage('linux') {
            steps { 
                echo 'test'
                echo 'changes for new PR'  
            }
        }
        
    }
}
