# Refactoring to ActiveRecord: Step 2

Thursday, we worked through refactoring the rest of the application into ActiveRecord.

Order of operations:

1. Refactor all database access out of the tests.
  1. We started by searching in the test directory for all manual database statements.
    * We then started by refactoring all of the `select count(*) from table_name` statements into a new `count` method on our model classes.
    * See: https://github.com/elizabrock/nss-capstone-2-example/commit/3be7f511a50751c3a74ea6aa7f1ce9a3e254f37a
  2. We then cleaned up the last of the database access from the tests. In doing so, we found, tested, and fixed a bug.
    * See: https://github.com/elizabrock/nss-capstone-2-example/commit/1cb7b715f432fb97fd0b2c134c37a04f70c21c5a
2. We then started refactoring all of the model classes into ActiveRecord.
  1. The Category Model
    1. First, we commented out the Category class.
    2. And then we ran the unit tests just for the Category class (`ruby test/test_categories.rb`), which we expected to fail
    3. We then let the failing Category unit tests drive us to implement the Category class in ActiveRecord.
  2. The Purchase Model
    1. Next, we followed the same steps from the Category class to refactor the Purchase class.
  3. The Integration tests
    1. Finally, knowing that the two model classes were now working (to the best of our knowledge), we ran `rake`, hoping that it would pass.
    2. We then focused on one failing integration test at a time and implemented the necesary code to fix it.
      * Note: When we found untested model methods, we wrote tests in the model *and then* implemented them in the model.
3. Profit!
  1. At this point, `rake` should pass.
  2. Commit everything and push it up!

