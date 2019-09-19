node {
  stage('Test') {
    sh 'date'
  }
  stage('Trigger Demo Job') {
    build (
      job: 'demogithub',
      parameters: [string(name: 'BRANCH', value: '--git-ref=dev')]
    )
  }
}
