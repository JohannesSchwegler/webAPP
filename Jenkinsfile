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
         bat 'mvn install'
      }
    }
    
    stage('Deloy') {
      steps {
       deploy adapters: [tomcat9(credentialsId: '85fb946a-3f6e-4ba8-9064-a91bfb6e5455', path: '', url: 'http://localhost:8081')], contextPath: 'sample.war', war: '**/*.war'
      }
    }
    
  }
}
