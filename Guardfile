# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#

# require 'growl'

# notification :growl

guard 'shell' do
  watch(/(.*)/) do |m|
    `echo #{m[0]} && growlnotify -a Dropbox Data Mustard -m "File updated: #{Pathname.new(m[0])}"`
  end
end