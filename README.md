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
        <li><a href="#getting-info">Getting info</a></li>
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
  </ol>
</details>



<!-- Imperative -->
## Imperative


Imperative way to run commands with kubectl.


### Getting info

get info of xy



<!-- Declarative -->
## Declarative

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Creating Pods

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Controllers and Services

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


## Templates
Please contribute using the templates below.
* Showing files
<pre><code>
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
</code></pre>



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Kubernetes Documentation](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [CKA exam description](https://www.cncf.io/certification/cka/)
