<!-- Sourcegraph -->
## Sourcegraph

[![Product Name Screen Shot][product-screenshot]](https://sourcegraph.eks.qcinternal.io/search)

Sourcegraph is a code search and intelligence tool for developers. It lets you search and explore all of your organization’s code on the web, with integrations into your existing tools.



<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.


### Prerequisites

Make sure you are in the right cluster and namespace before updating Sourcegraph.
* Cluster: Main-production-red-usw2 | Namespace: Sourcegraph
  ```sh
  kubectl config set-context $(kubectl config current-context) --namespace=sourcegraph
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/sourcegraph/deploy-sourcegraph
   ```
2. Delete all hidden .git files/directory
   ```sh
   ls -la
   ```
3. Configure codeintel-db.Deployment.yaml images to the newest version

*pgsql
*PG_EXPORTER_EXTEND_QUERY_PATH

4. Configure sourcegraph-frontend.deployment.yaml images to the newest version

*frontend
*jaeger-agent

5. Configure github-proxy.Deployment.yaml images to the newest version

*github-proxy
*jaeger-agent

6. Configure gitserver.Statefulset.yaml images to the newest version

*gitserver
*jaeger-agent

7. Configure indexed-search.StatefulSet.yaml images to the newest version

*zoekt-webserver
*zoek-indexserver

8. Configure minio.Deployment.yaml image to the newest version

*MINI_SECRET_KEY

9. Configure pgsql.Deployment.yaml images to the newest version

*correct-data-dir-permissions 
*container
*PG_EXPORTER_EXTEND_QUERY_PATH

10. Configure worker.deployment.yaml image to the newest version

*fieldPath: metadata.name

11. Configure query-runner.Deployment.yaml images to the newest version

*query-runner

12. Configure redis-cache.Deployment image to the newest version

*redis-store

13. Configure repo-updater.Deployment.yaml images to the newest version

*repo-updater
*jaeger-agent

14. Configure searcher.Deployment.yaml images to the newest version

*CACHE_DIR  
*jaeger-agent

15. Configure work.Deployment.yaml image to the newest version

*metadata.name


```js
   const API_KEY = 'ENTER YOUR API';
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [] Feature 1
- [] Feature 2
- [] Feature 3
    - [] Nested Feature

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email@email_client.com

Project Link: [https://github.com/github_username/repo_name](https://github.com/github_username/repo_name)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
