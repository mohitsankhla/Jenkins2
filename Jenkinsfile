pipeline 
{
    agent any
    tools{
        maven "MAVEN_HOME"
    }

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
                git 'https://github.com/mohitsankhla/Jenkins2.git'
                echo 'This is stage for building the project'
                bat 'mvn clean'
            }
        }

        stage('Test') 
        {
            steps
            {
                git 'https://github.com/mohitsankhla/Jenkins2.git'
                echo 'This is stage for Test Execution'
                bat 'mvn clean'
            }
        }
    }
}
