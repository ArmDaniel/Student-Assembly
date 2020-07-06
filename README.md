## Student Assembly

For Demo purposes:  

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Motanovici/Student-Assembly)

Video Demo: [Student Assembly](https://youtu.be/z1FWUiJyfWQ)

---

#### Justification and Thought Process

Being my first time using the NEAR protocol, I decided to follow the 'Guest Book' template as it fitted my goals best.  
This application is meant to give students a way to express their thoughts and concerns at their University without
fear of censorship.

I shall further document the process, deciding which idea is feasible and what modifications have been made. 
-Daniel (23.06.2020)

---

The application currently provides the student's University name ,a timestamp and an UUID for clear distinction and future grouping(by interests or such).

As I was developing the dApp, its importance became clear: it can provide students with a means to share ideas and express problems from their communities in a transparent way. It is also able to let them organize their content based on interests, such that information overload is not a problem. Also, placed in the current context and the advancement of technology, this application can reach out to students worldwide , no matter of their social status or other prejudicial factors.

Being built using the NEAR protocol, it ensures everything is stored permanently and cannot be altered. Censorship is done away with.

Taking into consideration how many innovating ideas students around the globe have and how they can change their community, such an application comes as a helpful tool to further express all that creative potential. Last but not least, any problems can be dealt with directly on the platform and their authenticity is verified by students from the community. This can be done via NEAR tokens, which would allow students to vote/downvote anything that is posted on the platform.Thus, tokens granted by others based on quality and originality establish influence. 

I plan on making further research using this application by distributing it among colleagues in my University and write a Whitepaper based on the results. 


-Daniel (06.07.2020)

---

A complete Snyk scan has been made and the dApp was deemed as safe.

[![Known Vulnerabilities](https://snyk.io/test/github/Motanovici/Student-Assembly/badge.svg?targetFile=package.json)](https://snyk.io/test/github/Motanovici/Student-Assembly?targetFile=package.json)

---

Guest Book
==========

[![Build Status](https://travis-ci.com/near-examples/guest-book.svg?branch=master)](https://travis-ci.com/near-examples/guest-book)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/near-examples/guest-book)

<!-- MAGIC COMMENT: DO NOT DELETE! Everything above this line is hidden on NEAR Examples page -->

Sign in with [NEAR] and add a message to the guest book! A starter app built with an [AssemblyScript] backend and a [React] frontend.


Quick Start
===========

To run this project locally:

1. Prerequisites: Make sure you have Node.js ≥ 12 installed (https://nodejs.org), then use it to install [yarn]: `npm install --global yarn` (or just `npm i -g yarn`)
2. Install dependencies: `yarn install` (or just `yarn`)
3. Run the local development server: `yarn dev` (see `package.json` for a
   full list of `scripts` you can run with `yarn`)

Now you'll have a local development environment backed by the NEAR TestNet! Running `yarn dev` will tell you the URL you can visit in your browser to see the app.


Exploring The Code
==================

1. The backend code lives in the `/assembly` folder. This code gets deployed to
   the NEAR blockchain when you run `yarn deploy:contract`. This sort of
   code-that-runs-on-a-blockchain is called a "smart contract" – [learn more
   about NEAR smart contracts][smart contract docs].
2. The frontend code lives in the `/src` folder.
   [/src/index.html](/src/index.html) is a great place to start exploring. Note
   that it loads in `/src/index.js`, where you can learn how the frontend
   connects to the NEAR blockchain.
3. Tests: there are different kinds of tests for the frontend and backend. The
   backend code gets tested with the [asp] command for running the backend
   AssemblyScript tests, and [jest] for running frontend tests. You can run
   both of these at once with `yarn test`.

Both contract and client-side code will auto-reload as you change source files.


Deploy
======

Every smart contract in NEAR has its [own associated account][NEAR accounts]. When you run `yarn dev`, your smart contracts get deployed to the live NEAR TestNet with a throwaway account. When you're ready to make it permanent, here's how.


Step 0: Install near-shell
--------------------------

You need near-shell installed globally. Here's how:

    npm install --global near-shell

This will give you the `near` [CLI] tool. Ensure that it's installed with:

    near --version


Step 1: Create an account for the contract
------------------------------------------

Visit [NEAR Wallet] and make a new account. You'll be deploying these smart contracts to this new account.

Now authorize NEAR shell for this new account, and follow the instructions it gives you:

    near login


Step 2: set contract name in code
---------------------------------

Modify the line in `src/config.js` that sets the account name of the contract. Set it to the account id you used above.

    const CONTRACT_NAME = process.env.CONTRACT_NAME || 'your-account-here!'


Step 3: deploy!
---------------

One command:

    yarn deploy

As you can see in `package.json`, this does two things:

1. builds & deploys smart contracts to NEAR TestNet
2. builds & deploys frontend code to GitHub using [gh-pages]. This will only work if the project already has a repository set up on GitHub. Feel free to modify the `deploy` script in `package.json` to deploy elsewhere.



  [NEAR]: https://nearprotocol.com/
  [yarn]: https://yarnpkg.com/
  [AssemblyScript]: https://docs.assemblyscript.org/
  [React]: https://reactjs.org
  [smart contract docs]: https://docs.nearprotocol.com/docs/roles/developer/contracts/assemblyscript
  [asp]: https://www.npmjs.com/package/@as-pect/cli
  [jest]: https://jestjs.io/
  [NEAR accounts]: https://docs.nearprotocol.com/docs/concepts/account
  [NEAR Wallet]: https://wallet.nearprotocol.com
  [near-shell]: https://github.com/nearprotocol/near-shell
  [CLI]: https://www.w3schools.com/whatis/whatis_cli.asp
  [create-near-app]: https://github.com/nearprotocol/create-near-app
  [gh-pages]: https://github.com/tschaub/gh-pages
