# DevOps Bootcamp Website & Curriculum

WWU Version hosted at [wwudevops.github.io/website][WWU DevOps Website].

OSU Version hosted at [devopsbootcamp.osuosl.org][OSU DevOps BootCamp].

## Installing Dependencies

### Debian and Ubuntu
```
sudo apt-get install build-essential
sudo apt-get install libtiff4-dev libjpeg8-dev zlib1g-dev \
libfreetype6-dev liblcms2-dev libwebp-dev tcl8.5-dev tk8.5-dev python-tk \
python3-dev python3-setuptoolsi
```

### Fedora
```
sudo yum groupinstall "Development Tools" "Development Libraries"
sudo yum install libtiff-devel libjpeg-devel libzip-devel freetype-devel \
lcms2-devel libwebp-devel tcl-devel tk-devel
```
    
### Installing Python Libraries
```
sudo pip install virtualenv
git clone https://github.com/WWUDevOps/website.git
virtualenv website
cd website
```

Enter the virtual environment.
```
source bin/activate
```

Install the requirements.
```
pip install -r requirements.txt
```

## Building

Output lives in `build/` and the stuff you want to edit is in `source/`. Images
and things go in `source/static/`.

Slides will go to `build/slides`.

Built html is stores on the gh-pages branch of this repository to be hosted with GitHub pages, so clone that branch into the `build/html` directory with: 

```
~$: mkdir build/
~$: git clone https://github.com/wwudevops/curriculum --branch gh-pages --single-branch build/html
```

To preview roughly how it'll look on
[wwudevops.github.io/curriculum][WWU DevOps Curriculum].

To make html pages
```
make html
```

For changes to take effect they have to be committed and pushed upstream (remember the `build/html` is a separate branch that we're treating as it's own "repository".

Leave the virtual environment.
```
deactivate
```

<!-- Links -->
[WWU DevOps Website]: https://wwudevops.github.io/website
[WWU DevOps Slides]: https://wwudevops.github.io/slides
[OSU DevOps BootCamp]: http://devopsbootcamp.osuosl.org/en/latest/
