pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
                git 'https://github.com/mohitsankhla/Jenkins2.git'
                echo 'This is stage for building the project'
                bat 'mvn clean
            }
        }

        stage('Test') 
        {
            steps 
            {
                echo 'Test App'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'selenium3bymukesh@gmail.com'
    	}

    }
}
