@Library('wsutil')
import org.mcb.Wswrapper

node{


//z.checkOutFrom("git@github.com:MCardenasBlanco/tfs-plugin.git")
    echo "Initializing"
    echo "${env.BUILD_NUMBER}"
    //sleep 5
    echo "${env.BUILD_NUMBER}"
    
    def t = new org.mcb.Wswrapper()
    println t.response.httpResponse.statusCode
    
    }
