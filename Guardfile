# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#

require 'growl'
require "pathname"

# notification :growl

guard 'shell' do
  watch(/(.*)/) do |m|
    puts "----------"
    path = Pathname.new(m[0])
    puts "Pathname = #{path}"
    
    notification = Growl.new
    notification.appIcon = "Finder"
    notification.title = "Data Mustard"
    
    if path.exist?
      notification.message = "File updated: #{path}"
    else
      notification.message = "File deleted: #{path}"
    end
    
    notification.run
  end
end

# `growlnotify -a Finder Data Mustard -m "File updated: #{path}"`