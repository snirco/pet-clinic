pipeline {
  agent any
  
  tools {
    maven "Maven"
//     jdk "jdk8"
  }
  
  stages {
    stage("Build") {
      steps {
        echo "Build stage"
        git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
      }
    }
    
    stage("Test") {
      steps {
        echo "Test stage"
        sh 'mvn compile'
//           mvn test
      }
    }
  }
}
