pipeline {
    agent any 
    parameters{
        string(defaultValue: 'myDefaultParameter1', description: 'descriotion', name: 'MY_STRING_PARAM_1')
        string(defaultValue: 'myDefaultParameter2', description: 'descriotion', name: 'MY_STRING_PARAM_2')
         string(name: 'MY_STRING_PARAM', defaultValue: 'myDefaultValue', description: 'String parameter used for...')
    }
    stages {
        stage('Build') { 
            steps {
                sh "echo 'Dummy building...' " 
                sh "echo $MY_STRING_PARAM_1"
                sh "echo $MY_STRING_PARAM_2"
            }
        }
        stage('Test') { 
            steps {
                sh """
                echo "Prepare env"
                echo 'Dummy testing...' 
                """
            }
        }
    }
}
