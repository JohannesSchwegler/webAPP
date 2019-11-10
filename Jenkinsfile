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
         deploy adapters: [tomcat9(path: '', url: 'http://localhost:8081')], contextPath: 'rps', war: '**/*.war'
      }
    }
    
  }
}
