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
        git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
        sh 'mvn compile'
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
        
    stage("Package Image") {
      steps {
        echo "Package Image stage..."
        sh "docker build '${registry}'/'${$BUILD_NUMBER}'"
      }
    }
  }
}
