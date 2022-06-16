1.What is the Folder Structure of Helm Chart?
        Folder Structure of the Helm Charts are as follows:
        Chart.yaml contains all the information about the charts.
        LICENSE used in containing the License for the chart.
        README.md is a readable file.
        values.yaml used in configuring the values for the chart.
        values.schema.json is a schema used in imposing the structure of values.yaml file.
        charts/ used in containing charts which are depends on this chart.
        crds/ is a custom resource definition.
        templates/ are used in combining directory of templates with the values and in generating valid kubernetes manifest files.
        templates/NOTES.txt used in containing Short Usage Notes.
2. What does chart.yaml file contains ?
Ans. It contains a chart description.

3. How to insert a release name into YAML template ?
Ans. {{.Release.Name}}

4. How to test the template rendering in Helm without installing anything ?
Ans. helm install --debug --dry-run ./testchart

5.What is helm chart 
             Helm helps you manage Kubernetes applications — Helm Charts help you define, install,
              and upgrade even the most complex Kubernetes application. 
            Charts are easy to create, version, share, and publish 
6.Chart Hooks
                pre-install	Executes after templates are rendered, but before any resources are created in Kubernetes
                post-install	Executes after all resources are loaded into Kubernetes
                pre-delete	Executes on a deletion request before any resources are deleted from Kubernetes
                post-delete	Executes on a deletion request after all of the release's resources have been deleted
                pre-upgrade	Executes on an upgrade request after templates are rendered, but before any resources are updated
                post-upgrade	Executes on an upgrade request after all resources have been upgraded
                pre-rollback	Executes on a rollback request after templates are rendered, but before any resources are rolled back
                post-rollback	Executes on a rollback request after all resources have been modified
                test	Executes when the Helm test subcommand is invoked ( view test docs)
7.
