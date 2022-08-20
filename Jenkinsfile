pipeline {
    agent {
    node {
        label 'slave1'
    }
 
}
tools {
            maven '3.5.4'
}

    stages {
      stage('clean up') {
            steps {
                echo 'Hello build dir'
                deleteDir()
            }
        }
        stage('build') {
            steps {
                 #dir('simple-java-maven-app'){
                    sh("mvn clean install")
                 }
            }
        }
        stage('test') {
            steps {
                 #dir('simple-java-maven-app'){
                    sh("mvn test")
                 }
            }
        }
    }
}
