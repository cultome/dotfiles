# Dotfiles

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/dotfiles`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Install the gem

    $ gem install dotfiles

## Usage

Start by initializing the folder structure and config file using:

    $ dotfiles init

Then you can start adding files to control using

    $ dotfiles add <path to file>

`dotfiles` will do 3 things:

 1. Backup you file in the same directory and same name, just appending `.backup` postfix.
 2. Move you file into `dotfiles` store (defaults to `~/.dotfiles/store`) and change its name to avoid collisions.
 3. Create a symbolic link from the moved file to the original location

 You can backup the files under `dotfiles` control by two mean: zip them o git-version them.


    $ dotfiles backup folder/to/store/zipfile

For version files in git, first is required to set the repository to use

    $ dotfiles config gitrepo git@github.com:cultome/dotfiles.git # or https://github.com/cultome/dotfiles.git
    $ dotfiles push


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/dotfiles. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/[USERNAME]/dotfiles/blob/master/CODE_OF_CONDUCT.md).

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Dotfiles project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/dotfiles/blob/master/CODE_OF_CONDUCT.md).
