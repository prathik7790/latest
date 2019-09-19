node {
  properties ([
    parameters ([
    string(name: 'BRANCH', defaultValue: '', description: 'DownStream Branch'),
    ])
  ])
  stage('Test') {
    sh 'date'
  }
  stage('Trigger Demo Job') {
    //build job: 'demogithub'
    //parameters: [string(name: 'BRANCH_NAME', value: params.BRANCH.toString())]
build job: 'demogithub', parameters: [[$class: 'StringParameterValue', name: 'BRANCH_NAME', value: params.BRANCH.toString()]]
  }
}
