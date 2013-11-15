## Bookworm API

These Python scripts make up the API used with the [Bookworm GUI](https://github.com/econpy/BookwormGUI) and can also be used as a standalone tool to query data from your database created by [Presidio](https://github.com/bmschmidt/Presidio).

### General Description
`dbbindings.py` gets called by the Bookworm GUI and executes `APIimplementation.py`, which selects data for the bookworm from the MySQL database location defined in `knownHosts.py`.


### Installation

On Ubuntu, you can simply run the `Makefile`:

```bash
sudo make ubuntu-install
```

However, you may wish to open the Makefile and see what is going on for yourself. The idea is to move the 3 python scripts to your cgi-bin, make them executable, and make the Apache user the owner of the files.

### Usage
Each bookworm on your system must have an entry in the `general_prefs` dictionary in knownHosts.py. This tells the API where to look for the data for a particular bookworm. The benefit of this setup is that you can have your webserver on one server and the database on another server.
