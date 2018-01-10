pipeline{
    agent any
    stages{
       
        stage('MacOSX') {
            steps{ echo 'test'
                 echo 'change in branch'
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
