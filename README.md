# homebrew-notes
These are my personal notes on how to use Homebrew effectively. Perhaps they may be useful to you

# Initial installation
I've added a script, `install_homebrew`, that tries the official install method if possible,
then falls back to the alternative manual method otherwise.

## Making a PR
*Definitely* read https://docs.brew.sh/How-To-Open-a-Homebrew-Pull-Request several times.

## Building a bottle
```sh
# First install without running post-install
brew install --build-bottle <formula>

# Make the bottle, recording the necessary details
# (<root_url> is for hosting outside Homebrew)
brew bottle --json [--root-url <root_url>] <formula>

# Then run post-install
brew postinstall <formula>
```
