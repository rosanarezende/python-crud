pipeline {
  agent any

  stages { 
    stage ('Checkout') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'b89d5c15-241c-418e-a8ae-6a4b1d19499b', url: 'https://github.com/rosanarezende/python-crud.git']]])
      }
    }

    stage('Build') {
      steps {
        git branch: 'main', credentialsId: 'b89d5c15-241c-418e-a8ae-6a4b1d19499b', url: 'https://github.com/rosanarezende/python-crud.git'
      }
    }

    stage ('Test') {
      steps {
        // nós podemos colocar aqui nossos testes
        echo 'The job has been tested'
      }
    }

    stage('Production') {
      steps {
        // nós podemos colocar as etapas pra colocar em produção
        echo 'The job has been put in production'
      }
    }
  }
}
