pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               sh "mkdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/Nithyareddy62/TicketBookingServiceJunitTesting.git"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
