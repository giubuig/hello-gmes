---
toc: false
theme: "air"
---

<style>

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: var(--sans-serif);
  margin: 4rem 0 8rem;
  text-wrap: balance;
  text-align: center;
}

.hero h1 {
  margin: 2rem 0;
  max-width: none;
  font-size: 14vw;
  font-weight: 900;
  line-height: 1;
  background: linear-gradient(30deg, var(--theme-foreground-focus), currentColor);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero h2 {
  margin: 0;
  max-width: 34em;
  font-size: 20px;
  font-style: initial;
  font-weight: 500;
  line-height: 1.5;
  color: var(--theme-foreground-muted);
}

@media (min-width: 640px) {
  .hero h1 {
    font-size: 90px;
  }
}

.text-align-center {
  text-align: center;
}

img.centered {
  display: block;
  margin-left: auto;
  margin-right: auto;
}

</style>

# Welcome
_We study how group-based models impact how we think about all sorts of contagion._

This is an experimental project that seek to combine group-based modeling and interactive visualization under the same roof.  

## Project structure

We take as starting point the [Observable Framework](https://observablehq.com/framework/project-structure) structure, but modify it a little to accomodate our simulation work. That is, on top of the Observable Framework project that mostly lives in `docs/` (see hidden summary below for authors' description), we have a project structure heavily inspired from the [Turing Way's repository structure](https://book.the-turing-way.org/project-design/project-repo/project-repo-advanced#example-with-every-possible-folder):

```ini
.
├─ data # Observable framework app
│  └─ raw       # import/raw data
│     ├── input_file_1.parquet
│     └─ input_file_2.parquet # file that is coming from excel sheet
├─ docs # Observable framework app
├─ src
│  ├─ InstitutionalDynamics.jl # gitsubmodules
│  ├─ processing.jl 
│  ├─ script-2-vacc.jl 
│  └─ source-sink-db.jl 
├─ .gitignore
├─ static # static resources (images and audio files)
├─ Makefile # A makefile to run the pipelind
├─ observablehq.config.js  # Observable Framework project config file
├─ package.json
├── results/   # static analysis
│   ├── result1.txt 
│   └── result2.txt
├─ README.md
└─ reqirements.txt
```

Our simulation code lives in `src/`. We have a subfolder called `RSB_submission` to play with code we written for our paper submitted to the _Royal Society B_. We output our simulation results in `results/`, which are then used by the app data loaders. We use the [Julia programming language](https://julialang.org/) as our backend. At the root-directory level, we have `Manifest.toml` and `Project.toml` to specify the environment to run the simulation.

<details><summary>How to get started with Observable Framework</summary>

## 

This is (also) an [Observable Framework](https://observablehq.com/framework) project. To start the local preview server, run:

```
npm run dev
```

Then visit <http://localhost:3000> to preview your project.

For more, see <https://observablehq.com/framework/getting-started>.

#### Project structure

A typical Framework project looks like this:

```ini
.
├─ docs
│  ├─ components
│  │  └─ timeline.js           # an importable module
│  ├─ data
│  │  ├─ launches.csv.js       # a data loader
│  │  └─ events.json           # a static data file
│  ├─ example-dashboard.md     # a page
│  ├─ example-report.md        # another page
│  └─ index.md                 # the home page
├─ .gitignore
├─ observablehq.config.js      # the project config file
├─ package.json
└─ README.md
```

**`docs`** - This is the “source root” — where your source files live. Pages go here. Each page is a Markdown file. Observable Framework uses [file-based routing](https://observablehq.com/framework/routing), which means that the name of the file controls where the page is served. You can create as many pages as you like. Use folders to organize your pages.

**`docs/index.md`** - This is the home page for your site. You can have as many additional pages as you’d like, but you should always have a home page, too.

**`docs/data`** - You can put [data loaders](https://observablehq.com/framework/loaders) or static data files anywhere in your source root, but we recommend putting them here.

**`docs/components`** - You can put shared [JavaScript modules](https://observablehq.com/framework/javascript/imports) anywhere in your source root, but we recommend putting them here. This helps you pull code out of Markdown files and into JavaScript modules, making it easier to reuse code across pages, write tests and run linters, and even share code with vanilla web applications.

**`observablehq.config.js`** - This is the [project configuration](https://observablehq.com/framework/config) file, such as the pages and sections in the sidebar navigation, and the project’s title.

#### Command reference

| Command           | Description                                              |
| ----------------- | -------------------------------------------------------- |
| `npm install`            | Install or reinstall dependencies                        |
| `npm run dev`        | Start local preview server                               |
| `npm run build`      | Build your static site, generating `./dist`              |
| `npm run deploy`     | Deploy your project to Observable                        |
| `npm run clean`      | Clear the local data loader cache                        |
| `npm run observable` | Run commands like `observable help`                      |

##

</details>

<br>

## The science of science of groups

In this collection of notebooks, we examine how array of institutional responses arises from group dynamics.

#### 1. Replicating Hébert-Dufresne et al. 2022

A group-based approach to model the co-evolution of some positive behavior (e.g., cooperation) and institutions aimed at fostering that behavior.

#### 2. Call for action

TO WRITE

---


