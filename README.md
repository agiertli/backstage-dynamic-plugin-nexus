##
This repository is for demonstrating Red Hat Developer Hub `Dynamic Plugins` functionality.

In particular it demonstrates `Nexus Plugin`.

### Prerequisite
- Provision `Supercharge Developer Experience: Openshift & Red Hat Developer Hub Workshop` catalog item in `demo.redhat.com` 
- Log into your OpenShift Cluster as `admin` user

### Step by step guide

- Install the Nexus Repository - `cd nexus-operator`
  - Install the nexus operator - `oc apply -f nexus.yaml` This commands can take up to 5 min to finish.
  - Retrieve Nexus `admin` user password - `oc exec deploy/example-nexusrepo-sonatype-nexus -- cat /nexus-data/admin.password` 
  - Retrieve Nexus URL: `oc get route nexus -o jsonpath='{.spec.host}{"\n"}'`
