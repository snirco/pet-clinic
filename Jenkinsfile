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
        echo "Compile stage..."
        sh 'ls'
        sh 'rm -rf origin'
        sh 'rm -rf project'
        sh 'ls'
        git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
//         sh 'mvn compile'
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
}
