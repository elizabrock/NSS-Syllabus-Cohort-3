# Today's assignment:

1. Read about user stories:

  * [http://www.virtual-genius.com/resources/User%20Stories%20Quick%20Reference%20Guide.pdf](http://www.virtual-genius.com/resources/User%20Stories%20Quick%20Reference%20Guide.pdf)
  * [http://www.boost.co.nz/blog/agile/user-stories/](http://www.boost.co.nz/blog/agile/user-stories/)
  * [http://www.boost.co.nz/blog/agile/acceptance-criteria/](http://www.boost.co.nz/blog/agile/acceptance-criteria/)
  * [http://www.nomad8.com/files/acceptance_criteria.php](http://www.nomad8.com/files/acceptance_criteria.php)

Those articles use a variety of specific approaches for the story format, but the general theme is all the same: who, what and why.

2. Write a set of user stories describing your features

Commit your list of user stories to your project in the doc directory (e.g. doc/user_stories.md) of your project
The user stories should look like:

<pre>
  As a [user or actor]
  In order to [accomplish goal X or achieve a given business value]
  I want to [perform an action]
</pre>

Example:

<pre>
  As a grocery shopper that has entered a few grocery trips into the application
  I want to get the average price I've paid for a particular item
  In order to know if the sale in the weekly flyer is any good.
  
  Usage: ./grocerytracker stats "Campbell's Chicken Soup"
  
  Acceptance Criteria:
  * Prints out average/min/max prices I've paid for that item
  * If the item can't be found, it prints out a list of items with similar names
</pre>
