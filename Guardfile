# Guardfile built by Meez ( http://github.com/paulczar/meez )
# for testing your chef cookbooks.

guard :rubocop, cli: '-r cookstyle' do
  watch(/.+\.rb$/)
  watch(%r{(?:.+/)?\.rubocop\.yml$}) { |m| File.dirname(m[0]) }
end

guard :foodcritic, cookbook_paths: '.', cli: ['--epic-fail', 'any'] do
  watch(%r{attributes/.+\.rb$})
  watch(%r{providers/.+\.rb$})
  watch(%r{recipes/.+\.rb$})
  watch(%r{resources/.+\.rb$})
  watch(/metadata\.rb$/)
end
