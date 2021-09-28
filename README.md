These Ansible playbooks can be used to renew bootstrap certificates in
OpenShift v3.x.  The manual process is described here:
https://access.redhat.com/solutions/3782361
<p>
This repository contains the following playbooks:
<p>
Primary playbook:<br>
---------------<br>
update-bootstrap-certificates.yml: update bootstrap certificates
<p>
Optional playbooks:<br>
---------------<br>
approve-certificates.yml: approve all pending certificate signing requests (CSR).<br>
delete-certificates.yml: delete all pending CSRs.<br>
<p>
Prerequisites:<br>
---------------<br>
You must be logged into the cluster (with oc login) prior to running the playbooks.
This user must be an administrator, with the cluster-admin role assigned.<br>
<p>
Note:<br>
---------------<br>
The update playbook will perform a rolling restart of the OpenShift API services
across all nodes.  As long as there is sufficient capacity (more than 1 node of
each type), there should be no outage in OpenShift availability.
