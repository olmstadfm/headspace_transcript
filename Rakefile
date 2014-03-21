require 'haml'
require 'ostruct'
task :generate_html do

     context = OpenStruct.new
     en = File.open('1.txt').readlines
     ru = File.open('1-tr.txt').readlines
     context.enru = en.zip(ru)
     puts Haml::Engine.new(IO.read('template.html.haml')).render(context)
     
end  
