def user_id
def group_id
node {
  user_id = sh(returnStdout: true, script: 'id -u').trim()
  group_id = sh(returnStdout: true, script: 'id -g').trim()
}

pipeline {
  agent { label 'docker' }
  stages {
    stage('commit_stage') {
      steps {
        echo 'user_id'
        echo user_id
        echo 'group_id'
        echo group_id
      }
    }
  }
}
