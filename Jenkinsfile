pipeline {
  agent any
  
  tools {
    maven "Maven"
//     jdk "jdk8"
  }
  
  stages {
    stage("Build") {
      steps {
        sh 'echo "Build stage..."'
        git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
        sh 'mvn compile'
      }
    }
    
    stage("Test") {
      steps {
        sh 'echo "Test stage..."'
        sh 'mvn test'
        sh 'mvn dependency:tree'
      }
    }
  }
}
