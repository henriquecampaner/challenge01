<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Challenge 02: Node.js concepts
</h3>

<p align="center">"Don't wait to plant, just be patient to reap"!</blockquote>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/rocketseat/bootcamp-gostack-desafios?color=%2304D361">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%2304D361">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/Rocketseat/bootcamp-gostack-desafios/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/rocketseat/bootcamp-gostack-desafios?style=social">
  </a>
</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">About the challenge</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Delivery</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">License</a>
</p>

## :rocket: About the challenge

In this challenge, you must create an application to train what you have learned so far in Node.js!

This will be an application to store repositories in your portfolio, which will allow the creation, listing, update and removal of the repositories, and also allow the repositories to receive "likes".

### Application template

To help you with this challenge, we have created a template for you that you should use as a github template.

The template is available at the following url: ** [Access Template] (https://github.com/Rocketseat/gostack-template-conceitos-nodejs) **

Now navigate to the created folder and open it in Visual Studio Code, remember to run the `yarn` command on your terminal to install all dependencies, and you will have something like this:

<p align="center">
  <img  src="./assets/nodejs-example.png">
</p>

### Application routes

Now that you have the template cloned, and ready to continue, you must open the app.js file, and complete where there is no code with the code to achieve the objectives of each route.

- **`POST /repositories`**: The route should receive `title`,` url` and `techs` within the body of the request, the URL being the link to the github of this repository. When registering a new project, it must be stored inside an object in the following format: `{id:" uuid ", title: 'Desafio Node.js', url: 'http: //github.com / ...' , techs: ["Node.js", "..."], likes: 0} `; Make sure the ID is a UUID, and always start the likes as 0.

- **`GET /repositories`**: Route that lists all repositories;

- **`PUT /repositories/:id`**: The route should only change the `title`,` url` and `techs` of the repository that has the` id` equal to the `id` present in the parameters of the route;

- **`DELETE /repositories/:id`**: The route must delete the repository with the `id` present in the route parameters;

- **`POST /repositories/:id/like`**: The route must increase the number of likes from the specific repository chosen through the `id` present in the route parameters, at each call of this route, the number of likes must be increased by 1;

### Specification of tests

In each test, you have a brief description of what your application must do in order for the test to pass.

For this challenge we have the following tests:

- **`should be able to create a new repository`**: For this test to pass, your application must allow a repository to be created, and return a json with the created project.

- **`should be able to list the repositories`**: For this test to pass, your application must allow an array to be returned with all the repositories that have been created so far.

- **`should be able to update repository`**: For this test to pass, your application must allow only the `url`,` title` and `techs` fields to be changed.

- **`should not be able to update a repository that does not exist`**: For this test to pass, you must validate in your update route whether the repository id sent by the url exists or not. If not, return an error with status `400`.

- **`should not be able to update repository likes manually`**: In order for this test to pass, you must not allow your update route to directly change the likes of this repository, maintaining the same number of likes that the repository already had before the update. That's because the only place that should update this information is the route responsible for increasing the number of likes.

- **`should be able to delete the repository`**: For this test to pass, you must allow your delete route to delete a project, and when deleting it, it returns an empty response, with status `204`.

- **`should not be able to delete a repository that does not exist`**: For this test to pass, you must validate on your delete route whether the repository id sent by the url exists or not. If not, return an error with status `400`.

- **`should be able to give a like to the repository`**: For this test to pass, your application must allow a repository with the given id to receive likes. The value of likes must be increased by 1 with each request, and as a result, return a json containing the repository with the number of likes updated.

- **`should not be able to like a repository that does not exist`**: For this test to pass, you must validate on your like route whether the repository id sent by the url exists or not. If not, return an error with status `400`.

## :calendar: Entrega

Esse desafio deve ser entregue a partir da plataforma Skylab, envie o link do repositório que você fez suas alterações. Após concluir o desafio, fazer um post no Linkedin e postar o código no Github é uma boa forma de demonstrar seus conhecimentos e esforços para evoluir na sua carreira para oportunidades futuras.

## :memo: License

This project is under the MIT license. See the archive [LICENSE](LICENSE.md) for more details.

---

Done with 💜 by Rocketseat :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
