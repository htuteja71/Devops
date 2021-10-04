pipeline{
    agent any
	environment {
		ARM_CLIENT_ID = "23101c39-455f-4b5f-9b33-ab76d68b4f7c"
		ARM_CLIENT_SECRET = "a76d18c1-9b73-43de-ac01-8e9856d6da32"
		ARM_TENANT_ID = "fc4cf7ec-2b33-4ccb-bf4f-dfdf72a2e9c6"
		AZURE_CLIENT_ID = "23101c39-455f-4b5f-9b33-ab76d68b4f7c"
		AZURE_CLIENT_SECRET = "a76d18c1-9b73-43de-ac01-8e9856d6da32"
		AZURE_TENANT_ID = "fc4cf7ec-2b33-4ccb-bf4f-dfdf72a2e9c6"

	}
    stages{
        stage('Terraform version info'){
            steps{
                sh '/usr/bin/terraform version'
            }
        }
        stage('Git'){
            steps{
                git 'https://github.com/htuteja71/Devops/'
            }
        }
        stage('terraform init'){
            steps{
                echo "++++++  Terraform Initilising "
                sh '/usr/bin/terraform init'
            }
        }
        stage('terraform plan'){
            steps{
                echo "++++++  Terraform Plan -out "
                sh '/usr/bin/terraform plan'
            }
        }
        stage('terraform apply'){
            steps{
                echo "++++++  Terraform apply "
                sh '/usr/bin/terraform apply --auto-approve'
            }
        }		
    }
}
