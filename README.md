# Annotator

![Media Ecology Project Image](/media/cropped-mep_banner511.png)

Annotator is a replacement video player for HTML5 videos which allows for 
viewing, creating, and modifying user-made annotations under the specification 
of the [Media Ecology Project](https://sites.dartmouth.edu/mediaecology/). 

This project is in an early alpha phase. As such, please note that it's still 
rough around the edges; documentation and clarifying information will be fleshed
out further as the project progresses.


## How to Use

You can use the pre-built set of files in the Releases once I figure out how 
Travis CI works; If you'd like to build your own, see the **How to Build** 
section below.

### Prerequisites

* [jQuery](https://jquery.com/)
* [jQuery UI](https://jqueryui.com/)

### Deployment

You will need to import the above prerequisites and the files from 
[/dist/](/dist/) on your page.

You can then use jQuery to reference a video object, and call `annotate()` on
it; the plugin will do the rest.

Example:
```
<script>
    $("video").annotate();
</script>
```

You can see a full example at [/testpage/](/testpage/).

### Styling

Information forthcoming.

### Known Issues

For some reason, the vertical offset of the annotations are wrong (slightly raised)
when the Chrome dev tools are open and the video is fullscreen. If anyone has an idea
why, please let us know.

## How to Build

This project is written in ES6 and transpiled by Babel and Browserify into a bundled file.

Note that this project was developed with [Visual Studio Code](https://code.visualstudio.com/). 
It is highly recommended that you also use this.

### Prerequisites

* NPM

### Installation

1. Install the dependencies with NPM.

```
npm install
```

### Building

Building is done using Grunt. In Visual Studio Code, you can run a task with 
`task taskName`.

Tasks:

* `build`   - Bundles the source files into [/dist/](/dist/).
* `preview` - Sets up live development environment with BrowserSync. Loads 
              [/testpage/](/testpage/).

## Built With

* Grunt
* Babel
* Browserify

## Contributing

Right now the project is in an early alpha phase, and is not open for pull requests
due to the rapid state of change. We will revisit this when things settle down.

## Authors

* **Jonathan Cole** - *VEMILab* - [joncole.me](http://www.joncole.me)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details