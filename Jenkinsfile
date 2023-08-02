node {
  stage('CHECKOUT SCM') {
    git 'https://github.com/subbhash/angular-app.git'
  }
  stage('install node modules') {
    sh "npm install"
  }
  stage('Test') {
    sh "npm run test-headless"
  }
  stage('Build') {
    sh "npm run build --prod"
  }
  stage('copy') {
    sh "cp -a /var/lib/jenkins/workspace/angular-app-1/dist/hello-world/. /var/www/hello-world/html/"
  }
}
