pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
      git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/mohankumar-putta/jenkins-ansible.git'
       }
 }

 stage('Execute Ansible'){
  steps{   
       ansiblePlaybook credentialsId: 'jenkins', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
      }
 }
    }

}
  
