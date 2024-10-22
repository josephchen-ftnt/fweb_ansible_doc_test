View docs generated by this project: https://ansible-galaxy-fortiweb-docs.readthedocs.io


for local tests, run 

```sh
make html
cd _build/html
python3 -m http.server 8080
```

open http://localhost:8080 to view the generated docs


Testing Ansible Galaxy FortiADC Collection Documentation:

1. Run ./mktar.sh <Project_NAME> at root directory.
2. Go to output and check whether "fortiadc.galaxy.document.<Project_NAME>.tar" exists
3. Login to your github account, and create a new repository.
4. Upload "fortiadc.galaxy.document.<Project_NAME>.tar" into your personal github repository created in step 3.
5. Go to https://readthedocs.org/dashboard/, register and login.
6. Click "Import a project", and use the the address of your personal github repository created in step 4, and choose the correct branch.
7. Click "Build version" and check the result.

For each new ansible release, increase the value of "version" in doc/.readthedocs.yaml by 1.

For versions number change:

1. edit the doc/docs/index.rst by finding the following content:
"Welcome to Ansible Galaxy FortiADC Collection Documentation !", and change the version number to the latest one.
2. edit the doc/docs/release.rst, and add information of new release.
3. edit the doc/docs/version.rst, and add new table entry for the released version.
4. edit the fortiadc/galaxy.yml by finding the following content: 
documentation: "https://ansible-galaxy-fortiadc-docs.readthedocs.io/en/galaxy-", and change the url to point to the latest version.