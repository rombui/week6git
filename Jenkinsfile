pipeline{
  agent any
  stages{
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
        sh 'terraform destroy --auto-approve -no-color'
      }
    }
  }
}

