node {
  stage('Test') {
    sh 'date'
  }
  stage('Trigger Demo Job') {
    build (
      job: '../../demogithub'
    )
  }
}
