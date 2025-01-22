Suppose our application is coded with Python. For the CI linting step we could use Pylint. For testing we can use Pytest.
In this case as our language is Python and it is an interpreted languange, the build stage mainly revolves around test execution. We should take into account
all the Python dependencies that don't come with the base Python. We should keep the requirements updated for example with
Poetry.

We can setup the CI for example with CircleCI or TravisCI, which are well-suited for Python projects. CircleCl monitors GitHub and launches builds
after a new commit. It tests the builds automatically in Docker containers or a virtual machine and deploys passing builds
to the target environment. Similarly if we use TravisCL, it too can be linked with GitHub so that it receives a notify
whenever a new commit is made. It can be configured to run on different machines with different software installed.

Our application seems to be a small project. In this case we could use a cloud-based CI environment to save money
and hassle as the configuration should be fairly straightforward. We could then also deploy directly from the cloud.
This decision depends on whether our project has some special requirements for example GPU and if the project is goint
to be scaled up significantly later on.
