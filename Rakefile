require 'rubygems'
require 'closure-compiler'

task :default => :minify

desc 'Minify peity.js.'
task :minify do
  minified = Closure::Compiler.new.compile(File.open('src/peity.js', 'r'))

  File.open('src/peity.min.js', 'w') do |f|
    f.write minified
  end

  puts 'Done.'
end
