pipeline {
  agent { label 'taosdata-app' }
  environment {
   ANSIBLE_PRIVATE_KEY=credentials('ansible') 
  }
  stages {
    stage('Hello') {
      steps {
        sh 'ansible-playbook -i inventory/hosts --private-key=$ANSIBLE_PRIVATE_KEY hello.yml'
      }
    }
  }
}
