pipeline{
    agent any
        stages{
            stage('code checkout'){
                steps{
                   git branch: 'main', credentialsId: '8bd4e249-8844-4bcf-8610-94f8b28457e1', url: 'https://github.com/mohankumar-putta/jenkins-ansible.git'
                   echo "code checkout completed"
               }
            }
            stage('code build'){
                steps{
                    ansiblePlaybook credentialsId: 'user-2', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
                    echo "code build completed"
                }
            }
        }
}

  
