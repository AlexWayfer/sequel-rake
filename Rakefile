# frozen_string_literal: true

require "bundler/gem_tasks"
require "rake/testtask"

Rake::TestTask.new do |t|
  t.pattern = "test/**/*_test.rb"
  t.libs.push "test"
end

namespace :test do
  task :coverage do
    ENV["COVERAGE"] = "true"
    Rake::Task["test"].invoke
  end
end

task default: :test
