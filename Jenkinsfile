@Library('pipeline-library-v1.0')_
node {
 def url = sh(returnStdout: true, script: 'git config remote.origin.url').trim()
 echo "${url}"
}

