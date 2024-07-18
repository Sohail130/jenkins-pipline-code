pipeline {
    agent any
pipeline {
    agent none
    stages {
        stage('Run on both nodes') {
            parallel {
                stage('Build on node1') {
                    agent { label 'tp' } // Replace 'node1' with your actual node label
                    stages {
                        stage('Building') {
                            steps {
                                echo 'The Code will now be built into an artifact on node1'
                            }
                        }
                        stage('Artifact Archiving') {
                            steps {
                                echo 'The Artifact will be uploaded to an artifact repository on node1'
                            }
                        }
                        stage('Testing') {
                            steps {
                                echo 'The Artifact will be tested on node1'
                            }
                        }
                        stage('Staging') {
                            steps {
                                echo 'The Artifact is staged onto the staging server on node1'
                            }
                        }
                        stage('Deploy') {
                            steps {
                                echo 'The software will now be deployed on node1!'
                            }
                        }
                    }
                }
                stage('Build on node2') {
                    agent { label 'tp' } // Replace 'node2' with your actual node label
                    stages {
                        stage('Building') {
                            steps {
                                echo 'The Code will now be built into an artifact on node2'
                            }
                        }
                        stage('Artifact Archiving') {
                            steps {
                                echo 'The Artifact will be uploaded to an artifact repository on node2'
                            }
                        }
                        stage('Testing') {
                            steps {
                                echo 'The Artifact will be tested on node2'
                            }
                        }
                        stage('Staging') {
                            steps {
                                echo 'The Artifact is staged onto the staging server on node2'
                            }
                        }
                        stage('Deploy') {
                            steps {
                                echo 'The software will now be deployed on node2!'
                            }
                        }
                    }
                }
            }
        }
    }
}
