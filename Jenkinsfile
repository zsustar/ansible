pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'This is Saju\'s Pizza'
      }
    }
    stage('zip the file') {
      steps {
        sh 'zip -r twentysixteen.zip twentysixteen'
      }
    }
    stage('Deploy New Theme') {
      steps {
        ansiblePlaybook(playbook: '/apps/ansible/copy_wp/site.yml', colorized: true, credentialsId: 'MIT-Lab-Star', inventory: '/apps/ansible/copy_wp/dev.host', extras: '--extra-vars \'{"wp_theme":"twentysixteen"}\' --extra-vars \'{"wp_theme_file":"twentysixteen.zip"}\'')
      }
    }
    stage('Test Done') {
      steps {
        echo 'WP has been updated successfully!'
      }
    }
  }
}