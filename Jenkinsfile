node {
    def mvnHome = tool 'M3'

    stage('Checkout') {
        checkout scm
    }

    stage('Build') {
        sh "${mvnHome}/bin/mvn clean install -DskipTests"
    }

    stage('Test') {
        sh "${mvnHome}/bin/mvn test"
    }

    mail to: staskolodyuk@gmail.com, body: 'Build has successfully passed'

}
