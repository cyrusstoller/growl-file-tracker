# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#

# require 'growl'
require "pathname"

# notification :growl

guard 'shell' do
  watch(/(.*)/) do |m|
    puts "----------"
    path = Pathname.new(m[0])
    puts "Pathname = #{path}"
    
    if path.exist?
      `growlnotify -a Dropbox Data Mustard -m "File updated: #{Pathname.new(m[0])}"`
    else
      `growlnotify -a Dropbox Data Mustard -m "File deleted: #{Pathname.new(m[0])}"`
    end
  end
end