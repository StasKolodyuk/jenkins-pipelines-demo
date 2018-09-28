node {
   checkout scm

   def mvnHome = tool 'M3'

   stage('Build') {
      sh "${mvnHome}/bin/mvn clean install -DskipTests"
   }

   stage('Unit Tests') {
      sh "${mvnHome}/bin/mvn test"
   }

   mail to: 'staskolodyuk@gmail.com', body: 'Build has successfully passed'

}