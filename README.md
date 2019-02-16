jekyll-gulp-sass-browser-sync
=============================

## Preparation

1. [Jekyll](http://jekyllrb.com/) - `$ gem install jekyll`
2. [NodeJS](http://nodejs.org) - download and install.
3. jump into a directory of repo, run `npm install`
4. [GulpJS](https://github.com/gulpjs/gulp) - `$ npm install -g gulp`
    then run `$ gulp`, browser shown.
5. Jade - `$ npm install gulp-jade --sav-dev`
6. create jade in gulpfile.js and add it to watch task
    
    ```javascript
    var jade = require('gulp-jade');
    /*
    * gulp staff
     */
    gulp.task('jade', function () {
        return gulp.src('_jadefiles/*.jade')
            .pipe(jade()) //chane jade to html
            .pipe(gulp.dest('_includes'));
    });
    
    /**
     * Watch scss files for changes & recompile
     * Watch html/md files, run jekyll & reload BrowserSync
     */
    gulp.task('watch', function () {
        gulp.watch('_jadefiles/*.jade', ['jade']);
    });
    ```
7. check if gulp running right with jade `$ gulp jade`
8. [normalize.css](http://necolas.gihub.io/normalize.css/) - download and save into assets/css/0-tools
9. bourbon - in the direction, `$ gem install bourbon`, `$ bourbon install`


