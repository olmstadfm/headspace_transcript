require 'haml'
require 'ostruct'

task :generate_html do

     context = OpenStruct.new
     en = File.open('1.txt').readlines
     ru = File.open('1-tr.txt').readlines
     context.enru = en.zip(ru)
     context.last_update = Time.now.strftime("%Y-%m-%d %H:%M:%S")
     puts Haml::Engine.new(IO.read('template.html.haml')).render(context)
     
end  
