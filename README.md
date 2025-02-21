# edruzin.me

Personal website

## Development

```bash
# install asdf
# docs: https://asdf-vm.com/guide/getting-started.html
brew install asdf

asdf plugin add ruby
brew install openssl@3 readline libyaml gmp

asdf install
asdf reshim
gem install bundler

# install dependencies
bundle install

# run development server
bundle exec jekyll serve
```

## License

The code is licensed under MIT license ([LICENSE-CODE.md](LICENSE-CODE.md)). All images in the `images` folder are licensed under CC BY-SA 4.0 license ([LICENSE-IMAGES.md](LICENSE-IMAGES.md)).
