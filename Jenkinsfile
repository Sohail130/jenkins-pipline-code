pipeline {
    agent none
    stages {
        stage('Run on both nodes') {
            parallel {
                stage('Node1') {
                    agent { label 'tp' } // Replace 'tp' with your node1 label if different
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
                stage('Node2') {
                    agent { label 'tp' } // Replace 'tp' with your node2 label if different
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
