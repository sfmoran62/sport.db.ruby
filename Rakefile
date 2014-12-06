require 'hoe'
require './lib/sportdb/cli/version.rb'


Hoe.spec 'sportdb' do

  self.version = SportDbCli::VERSION

  self.summary = 'sportdb - sport.db Command Line Tool'
  self.description = summary

  self.urls    = ['https://github.com/sportdb/sport.db.ruby']

  self.author  = 'Gerald Bauer'
  self.email   = 'opensport@googlegroups.com'

  # switch extension to .markdown for gihub formatting
  #  -- Note: auto-changed when included in manifest
  self.readme_file  = 'README.md'
  self.history_file = 'HISTORY.md'

  self.extra_deps = [
    ['sportdb-models', '>= 1.10.1'],

    ['fetcher', '>= 0.4.4'],    ## check if included already in datafil ??
    ['datafile', '>= 0.1.1'],

    ### sportdb addons
    ## ['sportdb-keys'],
    ['sportdb-update'],
    ['sportdb-service'],

    ## 3rd party
    ['gli', '>= 2.12.2'],

    ## ['activerecord'],  # Note: will include activesupport,etc.
    ['sqlite3']
  ]

  self.licenses = ['Public Domain']

  self.spec_extras = {
    required_ruby_version: '>= 1.9.2'
  }

  self.post_install_message =<<EOS
******************************************************************************

Questions? Comments? Send them along to the mailing list.
https://groups.google.com/group/opensport

******************************************************************************
EOS
  
end
