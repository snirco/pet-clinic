pipeline {
  agent any
  
  environment {
    registry = "snirco"
  }
  
  tools {
    maven "Maven"
  }
  
  stages {
    
    stage("Docker Test") {
      steps {
        sh 'docker --version'
        sh 'docker ps'   
      }
    }
    
    stage("Compile") {
      steps {
        sh 'ls'
        echo "Compile stage..."
        sh 'mkdir test'
        dir("test") {
          git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
        }
        sh 'ls test'
        sh 'ls'
      }
    }
    
//     stage("Test") {
//       steps {
//         echo "Test stage..."
//         sh 'mvn test'
//       }
//     }
    
//     stage("Check Dependencies") {
//       steps {
//         echo "Check Dependencies stage..."
//         sh 'mvn dependency:tree'
//       }
//     }
    
//     stage("Test Build") {
//       steps {
//         sleep 120 
//         sh 'docker build . '
//       }
//     }
  }
  post { 
    always { 
      cleanWs()
    }
  }
}
