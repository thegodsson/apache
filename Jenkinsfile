def PROJECT = 'dev'

pipeline {
  agent { label 'master' }
  
  tools {
      oc 'oc'
  }
  
 
  stages {
    stage('SAY Hello') {
        steps {
            sh 'echo "Hello" '
        }
    }
    
    stage('Openshift New App APACHEJM') {
        steps {
            script {
                openshift.withCluster() {
                    openshift.withProject(PROJECT) {
                        openshift.newApp('httpd')
                    }
                }
                
            }
            
    
    
    
  }
}
}
}
