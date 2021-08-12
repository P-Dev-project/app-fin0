pipeline {
  agent any
  stages {
    stage('Log Tool Version ') {
      parallel {
        stage('Log Tool Version ') {
          steps {
            sh '''mvn --version 
git --version
java -version'''
          }
        }

        stage('Check for POM') {
          steps {
            sh 'mvn -f app-fin0/springboot2-jpa-crud-example/pom.xml <goals>'
            fileExists 'pom.xml'
          }
        }

        stage('') {
          steps {
            sh '''npm install






npm install -g @angular/cli@9.1.0'''
          }
        }

      }
    }

    stage('Build with Maven') {
      steps {
        sh 'mvn -f app-fin0/springboot2-jpa-crud-example/pom.xml <goals>'
        sh 'mvn clean install -DskipTests'
        dir(path: 'app-fin0/springboot2-jpa-crud-example/')
      }
    }

    stage('Post build Test') {
      steps {
        writeFile(file: 'Status.txt', text: 'Hey it worked!!!')
      }
    }

  }
}