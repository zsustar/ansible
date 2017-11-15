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
    stage('error') {
      steps {
        ansiblePlaybook(playbook: '/apps/ansible/copy_wp/site.yml', colorized: true, credentialsId: 'MIT-Lab-Star', inventory: '/apps/ansible/copy_wp/dev.host', extras: 'test')
      }
    }
  }
}