
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/quorumcontrol/dgit">
    <img src="dgit-black.png" alt="Logo" width="150" height="125">
  </a>

  <h3 align="center">dgit</h3>

  <p align="center">
    <b>dgit</b> is an open-source project built by <a href="https://www.tupelo.org/">Quorum Control</a> which combines
    the power of <br>git, the <a href="https://docs.tupelo.org/">Tupelo DLT</a> and <a href="https://siasky.net/">Skynet</a> from Sia.  <br>
    <b>dgit</b> uses decentralized ownership and storage to make it trivial to
    create a decentralized, shareable git remote of your project.<br>
    <b>dgit</b> accomplishes this without changing your GitHub workflow except that you can keep collaborating when it goes down.<br>
  </p>
</p>

<!-- GETTING STARTED -->
## Getting Started
With three simple steps you can create a decentralized mirror of your existing github project.
All changes will be automatically propogated to the mirror version and the git services you depend on will be there when you need them.

### Installation
A quick install using brew gets us started: 
`brew tap quorumcontrol/dgit && brew install dgit` <br>
Or skip the tap and directly install with: 
`brew install quorumcontrol/dgit/dgit`

### Usage
Next you are going to run the init command in each repo you want to make decentralized:
`dgit init`

This command does three things.<br>
1. <b>dgit</b> sets the appropriate remote urls in your repo's .git/config file.<br>
2. <b>dgit</b> creates a [ChainTree](https://docs.tupelo.org/docs/chaintree.html) which gets signed by the Tupelo DLT to specify ownership of the decentralized repo.<br>
3. <b>dgit</b> stores that repo on Skynet, the decentralized storage solution from Sia. 

From there you can proceed with normal git commands.<br>
If you ever want to pull from the mirror you can specify the mirror with a "dgit:".<br>
As an example:
`git clone dgit://your_username/repo_name`
<br>
If you want to keep your decentralized, shareable git remote in sync with your GitHub repo adding
a simple github rule as illustrated in [dgit-github-action](https://github.com/quorumcontrol/dgit-github-action) is all it takes.  Once completed your  dgit decentralized shareable remote will always be up to date and ready when you need it.<br>

### Built With

* [Git](https://git-scm.com/)
* [Tupelo DLT](https://docs.tupelo.org/)
* [Skynet](https://siasky.net/)

### Building
- Clone this repo.
- Run `make`. Generates `./dgit` in top level dir.

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- CONTACT -->
## Contact

If you have any questions or concerns please [hop into our developer chat](https://gitter.im/quorumcontrol-dgit/community) 
on gitter and we will be glad to help. 

Project Link: [https://github.com/quorumcontrol/dgit](https://github.com/quorumcontrol/dgit)
