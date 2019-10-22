pipline {
  agent { label 'master' }
  tools {
    maven 'Maven 3.6.2'
  }
  stages {
    stages('Source') {
      steps {
        git branch: 'master',
        url: 'https://github.com/TongThanaphon/BookStore.git'
      }
    }
    stages('Build') {
      steps {
        sh 'mvn compile'
      }
    }
    stages('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stages('Deploy') {
      steps {
        sh 'mvn spring-boot:run'
      }
    }
  }
}
