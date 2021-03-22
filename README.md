<!-- PROJECT LOGO -->
<br />
<p align="center">
    <a href="#kb-for-cka-exam">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
    </a>

<!-- Main -->
## KB for CKA exam



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#imperative">Imperative</a>
      <ul>
        <li><a href="#pods">Pods</a></li>
        <li><a href="#nodes">Nodes</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Declarative</a>
      <ul>
        <li><a href="#creating-pods">Creating Pods</a></li>
        <li><a href="#controllers-and-services">Controllers and Services</a></li>
      </ul>
    </li>
    <li><a href="#templates">Templates</a></li>
      <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<br />
<br />
<br />

<!-- Imperative -->
## Imperative


Imperative way to run commands with kubectl.


### Pods

* List pods showing their labels
<pre><code>kubectl get pod --show-labels</code></pre>

* List pods with specific label
<pre><code>kubectl get pod -owide --selector=$label</code></pre>

### Nodes
* Remove default taint from master nodes
<pre><code>kubectl taint nodes --all node-role.kubernetes.io/master-</code></pre>

* Add taint to a node
<pre><code>kubectl taint nodes node1 key1=value1:NoSchedule</code></pre>






<br />
<br />

<!-- Declarative -->
## Declarative
Declarative way to create, modify objects or anything in k8s.

### Creating Pods

* Create pod with taint
<pre><code>#example-yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
  labels:
    env: test
spec:
  containers:
  - name: nginx
    image: nginx
    imagePullPolicy: IfNotPresent
  tolerations:
  - key: "example-key"
    operator: "Equals"
    value: "example-value"
    effect: "NoSchedule"
</code></pre>


### Controllers and Services


## Templates
Please contribute using the templates below.
* Showing files
<pre><code>Please ...First line
...Second line
paste the file content here
</code></pre>

* One line commands
<pre><code>this is an example command</code></pre>

* Step-by-steps
1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```JS
   const API_KEY = 'ENTER YOUR API';
   ```



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Kubernetes Documentation](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [CKA exam description](https://www.cncf.io/certification/cka/)
