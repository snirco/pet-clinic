pipeline {
  agent any
  
  environment {
    registry = "snirco"
  }
  
  tools {
    maven "Maven"
  }
  
  stages {
    
    stage("Compile") {
      steps {
        echo "Compile stage..."
        sh 'mkdir test'
        dir("test") {
          git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
          sh 'mvn compile'
        }
      }
    }
    
    stage("Test") {
      steps {
        echo "Test stage..."
        dir("test") {
          sh 'mvn test'
        }
      }
    }
    
    stage("Docker Build") {
      steps {
        sh 'docker build .'
      }
    }
  }
  post { 
    always { 
      cleanWs()
    }
  }
}
