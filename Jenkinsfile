pipeline {
    agent any

    stages {

        stage('1. Build') {
            steps {
                echo 'Task: Compile and package the application source code into a deployable artifact.'
                echo 'Tool: Maven (mvn clean package)'
            }
        }

        stage('2. Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests to verify individual components work correctly, and integration tests to verify components work together as expected.'
                echo 'Tool: JUnit (unit tests) and Postman/Newman (integration tests)'
            }
        }

        stage('3. Code Analysis') {
            steps {
                echo 'Task: Analyse source code for bugs, code smells, and maintainability issues to ensure it meets industry coding standards.'
                echo 'Tool: SonarQube'
            }
        }

        stage('4. Security Scan') {
            steps {
                echo 'Task: Scan the codebase and dependencies for known security vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('5. Deploy to Staging') {
            steps {
                echo 'Task: Deploy the built application to a staging environment for pre-production testing.'
                echo 'Tool: AWS EC2 (staging instance) via AWS CLI / Ansible'
            }
        }

        stage('6. Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests against the staging environment to confirm the application behaves correctly in a production-like setting.'
                echo 'Tool: Postman/Newman'
            }
        }

        stage('7. Deploy to Production') {
            steps {
                echo 'Task: Deploy the verified application build to the production environment for end users.'
                echo 'Tool: AWS EC2 (production instance) via AWS CLI / Ansible'
            }
        }
    }
}