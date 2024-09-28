pipeline{
  agent any
  stages{
    stages {
        stage('Check Terraform Version') {
            steps {
                sh 'terraform --version'
            }
        }
    stage('init'){
      steps{
        sh 'terraform init -upgrade -no-color'
      }
    }
    stage('validate'){
      steps{
        sh 'terraform validate -no-color'
      }
    }
   stage('plan'){
      steps{
        sh 'terraform plan -no-color'
      }
    } 
    stage('apply'){
      steps{
        sh 'terraform apply --auto-approve -no-color'
      }
    }
  }
}
