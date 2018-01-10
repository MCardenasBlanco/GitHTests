pipeline{
    agent any
    stages{
       
        stage('MacOSX') {
            steps{ echo 'test'
                 echo 'change in branch'
                  echo 'commit one'
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
