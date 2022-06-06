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
          sh 'ls'
          sh 'mvn compile'
          sh 'ls'
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
    
//     stage("Check Dependencies") {
//       steps {
//         echo "Check Dependencies stage..."
//         sh 'mvn dependency:tree'
//       }
//     }
    
    stage("Test Build") {
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
