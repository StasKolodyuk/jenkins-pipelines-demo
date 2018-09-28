node {
   checkout scm

   def mvnHome = tool 'M3'

   stage('Build') {
      sh "${mvnHome}/bin/mvn clean install -DskipTests"
   }

   stage('Unit Tests') {
      sh "${mvnHome}/bin/mvn test"
   }

}