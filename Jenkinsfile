pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # Replace /PATH/TO/VENV with the actual path to your venv directory.
                # For example, if your venv is located in your project directory, it might be something like:
                # ${WORKSPACE}/venv/bin/activate
                # Here, WORKSPACE is a Jenkins environment variable that points to the root of the workspace.
                
                # Activate the virtual environment
                source /Users/vinwizard/Desktop/CMU/Sem4/MLiP TA/Recitation 6 Jenkins/mlip/bin/activate

                # Run pytest command within that environment.
                # You should have pytest installed within the virtual environment for this to work.
                pytest

                # Assuming pytest is the last command and you want the build to reflect the test status,
                # you don't need an 'exit' command. The build will succeed or fail based on pytest results.
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}