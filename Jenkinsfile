pipeline {
  agent {
      docker {
        image {'maven:3-alpine'
        args '-v /root/.m2:/roor/.m2'
       }
     }
     stages {
      stage ('Bui;d') {
        steps {
          sh 'mnv -B -DskipTests clean package'
       }
     }
   }
 }
      
        
        
