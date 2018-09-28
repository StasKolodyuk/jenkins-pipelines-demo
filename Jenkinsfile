node {
    checkout scm

    def mvnHome = tool 'M3'

    stage('Build') {
        sh "${mvnHome}/bin/mvn clean install -DskipTests"
    }

    stage('Test') {
        sh "${mvnHome}/bin/mvn test"
    }

    stage('Publish to Artifactory') {
        sh "${mvnHome}/bin/mvn package deploy:deploy"
    }
}
