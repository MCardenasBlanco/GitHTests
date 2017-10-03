
@Library('shared-sample')
import org.mcb.sample

@Library('wsutil')
import org.mcb.wsutil

node{
def z = new org.mcb.sample()

//z.checkOutFrom("git@github.com:MCardenasBlanco/tfs-plugin.git")
    echo "Initializing"
    echo "${env.BUILD_NUMBER}"
    //sleep 5
    echo "${env.BUILD_NUMBER}"
    
    def t = new org.mcb.wsutil
    println t.response.httpResponse.statusCode
    
    }
