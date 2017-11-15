pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'This is Pro Yan\'s PizzaHut'
      }
    }
    stage('zip the file') {
      steps {
        sh 'zip -r twentysixteen.zip twentysixteen'
      }
    }
  }
}