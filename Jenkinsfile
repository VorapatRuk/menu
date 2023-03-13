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
                    bat 'java -jar ./target/book-1.0.jar'
               }
          }
     }
}
