pipeline {
  agent any
  
  stages {
    stage("Build") {
      steps {
        echo "Build stage"
        git clone "https://github.com/spring-projects/spring-petclinic.git"
        mvn compile
      }
    }
    
    stage("Test") {
      steps {
          echo "Test stage"
          mvn test
      }
    }
    
    stage("Delpoy") {
      steps {
          echo "Delpoy stage"
      }
    }
  }
}
