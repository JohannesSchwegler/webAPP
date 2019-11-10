pipeline {
  agent any
  stages {
    stage('HelloWorld') {
      steps {
        echo 'Hello World'
      }
    }
    
    stage('Install') {
      steps {
         bat 'mvn clean install'
      }
    }
    
    stage('Deloy') {
      steps {
      deploy adapters: [tomcat9(credentialsId: '559d1539-ff3e-4079-917d-2e095ec8699f', path: '', url: 'http://localhost:8081/')], contextPath: 'sample', war: '**/*.war'
      }
    }
    
  }
}
