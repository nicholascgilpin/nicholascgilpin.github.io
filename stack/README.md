# Stack

I'm planning on living a long time; at least 20 or more years. However, I don't expect the organizations that maintain this technology stack to surivive as long. Therefore, I've archived the dependencies for my site here. 

## Quick Start

I'm forgetful, so here's how I set up my tools for new environments.

```bash     
    sudo apt-get install -y hugo git
    sudo apt-get install ./stack/linux/git-lfs_2.11.0_amd64.deb
    git lfs install
    sudo tar -C /usr/local/ -xzf stack/linux/go1.15.linux-amd64.tar.gz
    export PATH=$PATH:/usr/local/go/bin
    echo "export PATH=\$PATH:/usr/local/go/bin" >> $HOME/.profile

    git version
    go version
    hugo version
```

## Cheat Sheet
```bash
# Make  new site
hugo new site quickstart
cd quickstart/

# Download and enable theme
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
echo 'theme = "ananke"' >> config.toml

# Make post
hugo new posts/my-first-post.md

# Serve locally (use -D to show drafts)
hugo server

# Edit optional settings
nano config.toml
```