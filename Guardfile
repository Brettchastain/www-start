group :development do

  if File.exists?("./config.rb")
    # Compile on start.
    puts `compass compile --time --quiet`
    # https://github.com/guard/guard-compass
    guard :compass do
      watch(%r{(.*)\.s[ac]ss$})
    end
  end

  guard :livereload, :host => '127.0.0.1', :port => '35729', :grace_period => 0.5 do
    watch(%r{.+\.(css|js|html?|php|inc|theme)$})
  end

end
