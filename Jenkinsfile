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
    //echo "Triggering job for branch ${env.BRANCH_NAME}"
   // BRANCH_TO_TAG = env.BRANCH_NAME
    //build job: 'demogithub'
    //parameters: [string(name: 'BRANCH_NAME', value: params.BRANCH.toString())]
build job: 'demogithub', parameters: [[$class: 'StringParameterValue', name: 'BRANCH_NAME', value: params.BRANCH.toString()]]
  }
}
/*echo "Triggering job for branch ${env.BRANCH_NAME}"
                    BRANCH_TO_TAG=env.BRANCH_NAME.replace("/","%2F")
                    build job: "../my-relative-job/${BRANCH_TO_TAG}", wait: false*/
