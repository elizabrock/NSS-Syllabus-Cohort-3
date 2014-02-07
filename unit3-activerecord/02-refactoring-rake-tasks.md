# Refactoring to ActiveRecord: Step 1

The first thing we did in preparing to move our projects to ActiveRecord is to move our database bootstraping tasks to use ActiveRecord and migrations.

See commits:

* https://github.com/elizabrock/nss-capstone-2-example/commit/5272760a94db635ff38c0d5e4e5aef067850fe4b
* https://github.com/elizabrock/nss-capstone-2-example/commit/0902de13a181c2993e5e801a9c35715a006f456a

Order of operations:

1. Add ActiveRecord to Gemfile
2. Update Rakefile to use ActiveRecord oriented rake tasks, subsituting database/environment information as necessary for your program
3. Create database migrations for your existing tables.  The file name should match the format shown in the example commits.
4. Delete your existing databases
5. Run `rake db:migrate`, which will set up your production database using the migrations.  This will also create db/schema.rb
6. Run `rake db:test:prepare`, which will bootstrap your test database
7. Make sure you updated the test section of your Rakefile so that it will run `rake db:test:prepare`
8. Run `rake`. It should pass. If it does not, figure out why!
9. Commit this refactor before moving on to the next steps.
