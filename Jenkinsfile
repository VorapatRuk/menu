pipeline {
     agent any
     stages {
          stage('Source') {
               steps {
                    git branch: 'master',
                        url: 'https://github.com/VorapatRuk/menu'
               }
          }
          stage('Build') {
               steps {
                    bat 'mvn package -DskipTests'
               }
          }
          stage('Test') {
               steps {
                    echo 'testing...'
               }
          }
          stage('Deploy') {
               steps {
                    bat 'java -jar ./target/menu-0.0.1-SNAPSHOT.jar'
               }
          }
     }
}
