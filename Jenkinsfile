node {
  stage('Test') {
    sh 'date'
  }
  stage('Trigger Demo Job') {
    echo "Triggering job for branch ${env.BRANCH_NAME}"
    BRANCH_TO_TAG = env.BRANCH_NAME
    build (
      job: 'demogithub/${BRANCH_TO_TAG}', wait: false
      //parameters: [string(name: 'BRANCH', value: '${BRANCH}')]
    )
  }
}
/*echo "Triggering job for branch ${env.BRANCH_NAME}"
                    BRANCH_TO_TAG=env.BRANCH_NAME.replace("/","%2F")
                    build job: "../my-relative-job/${BRANCH_TO_TAG}", wait: false*/
