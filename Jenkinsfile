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
         bat 'mvn deploy'
      }
    }
    
  }
}
