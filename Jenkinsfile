pipeline {
  agent {
      docker {
        image 'maven:3-alpine'
        args '-v /root/.m2:/roor/.m2 --network=host'
       }
     }
     stages {
      stage ('Bui;d') {
        steps {
          sh 'mvn -B -DskipTests clean package'
       }
     }
   }
 }

