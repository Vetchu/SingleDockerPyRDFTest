node() {
    def myImg
    stage ("Build image") {
        // download the dockerfile to build from
        git 'gitea@localhost:Vetch/DockerBaseTest.git'

        // build our docker image
        myImg = docker.build 'DockerPyRDF'
    }
}