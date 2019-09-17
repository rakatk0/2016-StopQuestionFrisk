# Module 07: Final Projects

Our final week of MAP674 consists of a modest "final project" with three specific requirements listed below.

Note that the final deadline has been extended until **midnight on Tuesday, September 17th**.

The submission of the final deliverable will follow a final collective meeting via Zoom at **6 PM on Tuesday, September 17th**. Join us for this meeting prepared to briefly share your Notebook project with us via screen share and talk us through your process.

## Requirements

Follow the general guidelines below to meet the three requirements. If you have concerns about any of them or the timeline for the deliverable reach out to your instructor. The objective of this assignment, like the curriculum as a whole, is to benefit your personal and professional development. Note that the third requirement is optional but encouraged.

**Recommended:** Read through this document before beginning and ask for clarification.

### Requirement 1. Produce a finalized, clean Jupyter notebook

Choose one of your favorite datasets/notebooks from MAP674 (likely one you were working on for Module 06). Incorporate any feedback from your instructor and work to finalize the notebook, specifically in terms of outputting data to fulfill requirement 2 (below).

Notebook composition may vary depending on the goal of the data project and desired end map. However, consider the following for what constitutes a clean and effective Notebook:

- [ ] A meaningful title
- [ ] Notebook metadata (your name as the author, the date)
- [ ] Table of contents (optional)
- [ ] Sections delineated with good subtitles (h2/h3 tags or `##`/`###` in Markdown)
- [ ] Objectives of the Notebook and Notebook subsections written in Markdown cells (tell the reader what the cells are doing)
- [ ] Descriptions of the data metadata, preferably with links to the data source(s)
- [ ] Code comments within cells
- [ ] Removal of extraneous code cells, failed experiments, or error outputs

See this GeoPandas 101 Notebook by Mark Cruse (MS) for a good example:

https://github.com/MarkCruse/geopandas-101

Commit changes to your Notebook within the *map674-module-07-username* repository and push up to the remote for help and final submission. This Notebook should write data files into a data/ directory that a web map can then load (see example below).

### Requirement 2. Make a web map

The New Maps Plus curriculum is largely focused on web-based GIS and mapping (compared to other more GIS-specific programs). 

MAP674 provides training in the use of Python, Jupyter Notebooks, and various 3rd-party Python libraries for more fundamental tasks of data wrangling/cleaning, exploration, and preparation for consumption into a public-facing web map.

Within this *map674-module-07* repository you'll find a basic responsive web map template in the directory *leaflet-template/*, built with the Bootstrap framework. 

This template also loads the most recent version of the [Leaflet JS library](https://leafletjs.com/) and displays a basic map. It also included the [D3.js library](https://d3js.org/) for the purpose of making the AJAX request to load the data into the page.

Feel free to use this template to complete this requirement. You may also use your own web map page build and design and/or any other web mapping solutions with which you're familiar.

The objectives of this requirement are twofold:

1. To complete the "full-stack web mapping pipeline" process by demonstrating that data processed within Python can be outputted in a format suitable for then loading into a web map. The most practical solution for this is to output a GeoJSON file (< ~6MB) from your Notebook and plot this on a tiled slippy map using Leaflet (see basic example below). CSV files are also suitable for point-level data.
2. To refresh ourselves on JS web mapping (since we've been neck deep in Python and Jupyter notebooks for 9 weeks now).

We don't have a lot of time to build a complicated web map with a polished user interface that accounts for best practices in UX design. Consider simply plotting and styling the data on the map as a minimal goal. If time permits, the addition of interactivity and UI controls is welcomed. Don't hesitate to ask your instructor for help.

Commit changes to this map as you develop and push to the remote for help from your instructor and for final submission.

### Requirement 3. A personal GitHub project repository

With the help of GitHub Classroom, New Maps Plus is able to generate individual private repositories for you from a template repository stored within our New Maps Plus GitHub account. Within MAP674, you've been cloning these down and pushing up changes to the remote for help and submissions. This works great in a educational learning environment like this one.

However, as many of us are aware a GitHub account with clean, well-documented repositories has become a de facto resume for those working within development. The objective of this requirement is that you have a "back-end" data processing component to add to your emerging GitHub "resume."

Once you've completed requirements 1 and 2 above:

1. Create a new repository on your personal GitHub account. Give this repository a meaningful name. Use hyphens instead of spaces and preferably all lowercase . For example: *github.com/rgdonohue/major-airports/*. Include a .gitingore file for Python and a license (GitHub offers these options when you create the repository).
2. Clone this repository to your local machine.
3. Copy your completed notebook and any associated data files and directory into this repository (see below for suggested directory structure).
4. Commit these changes and push to the remote.
5. Update the README.md file using Markdown with a brief description of data project. Explain to a reader what they're looking at and how to use/read the Notebook. Again see [Mark's example](https://github.com/MarkCruse/geopandas-101).

**Important**: your personal GitHub repository should **not** include the REAME.md contained within this *map674-module-07-username* repository (the one you're reading now), nor the *example/* or *leaflet-template/* directories also contained within.

Share a URL with your instructor via the Canvas Assignment when you're ready for submission.

**Note:** If for some reason your project is feeling under-developed and you wish to not host this publicly on your personal GitHub website at this time, talk with your instructor.

## Basic example

The following briefly outlines a basic workflow process we're aiming to cultivate within the program. The dataset here is simplified here for brevity.

**Step 01.** Begin by creating a directory within the *map674-module-07-username* directory and name it your anticipated personal GitHub repo name (see requirement 3).

Within that, create two directories, one for the map and one for the Notebooks. It is recommended that you have a *data* directory within each of these subdirectories as well (see the [recommended file directory structure below](#recommended-file-directory-structure)).

When requirements 1 and 2 are completed, you should be able to simply copy the contents of this single directory containing your project over to the local copy of your personal GitHub project, edit the README.md, and push up.

**Step 02.** Within your terminal, first update your package manager (e.g., `conda update conda`). 

Either create a new virtual environment for this project and install your desired Python packages (e.g., pandas, geopandas), or if you're using an existing virtual environment, update the packages within that (e.g., `conda update --all`).

**Step 03.** Within your *notebooks* directory, either create a new notebook or copy over an existing one for continued refinement and editing. The output of this notebook should be a GeoJSON or CSV file (written to the *map/data/* directory).

See the example notebook: [major-airports/notebooks/](major-airports/notebooks/).

**Step 04.** Adjust the parameters of your web map (e.g., center, zoom), load the data, and plot on the web map.

Here you'll likely want to simply copy the *leaflet-template/index.html* file into your *map/* directory. Be sure to open this file with a local web server (e.g., live-server) and within your text editor of choice (e.g. VS Code).

Also be sure to:

- [ ] Update the title of your web page (within the `<title></title>`) tags.
- [ ] Update the title of the page body and supplementary text/content
- [ ] Include the data source, author name, and date of the map

See the example map: [major-airports/map/](major-airports/map/).

### Recommended file directory structure

Example file directory structure:

- *major-airports/*
  - *README.md*
  - *map/*
    - *index.html*
    - *data/*
      - *airports-major.json*
  - *notebooks*
    - *airports.ipynb*
    - *data/*
      - *airports-raw.json*

As always, reach out for help on Slack or email your instructor through Canvas. We're on the home stretch! Keep up the awesome work.