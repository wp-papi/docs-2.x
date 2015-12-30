require 'middleman-gh-pages'
require 'fileutils'

task :default => [:build]

task :apigen do
  source = 'tmp/papi'
  target = 'source/apigen'

  if Dir.exists?(source)
    FileUtils.remove_dir(source)
  end

  if Dir.exists?(target)
    FileUtils.remove_dir(target)
  end

  sh "git clone git@github.com:wp-papi/papi.git #{source}"
  sh "cd #{source} && git checkout 2.x"
  sh "apigen generate --groups=none -s #{source}/src -d #{target}"

  FileUtils.remove_dir(source)
end
