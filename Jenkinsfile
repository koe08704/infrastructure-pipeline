node('linux') {
    git url: 'https://github.com/koe08704/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
    stage('GetInstances'){
        sh "aws ec2 describe-instances --region us-east-1"
    }
    stage('CreateInstance'){
        sh "aws ec2 run-instances --image-id ami-0371c52b98b0f3c73 --count 1 --instance-type t2.micro --key-name SEIS66503 --security-group-ids sg-0d10992ca6f46ec43 --subnet-id subnet-0e69fbf639059abdb --region us-east-1"  
    }
    
}
