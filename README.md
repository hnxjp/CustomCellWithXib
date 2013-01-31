CustomCellWithXib
=================

This is an easy way to make CustomCell with Xib.

How to use custom cell with xib file easily.
---------------------------------------------

1. Create a custom UITableViewCell Class. I named it CustomCell.
2. Create xib file for the custom UITableViewCell. I named it CustomCell.xib
3. Customize xib file like placing UILabels or something. And link them to UITableViewCell subclass - in this case, CustomCell.
4. Write two lines below to make UITableView handle CustomCell's instance.

viewDidLoad
<pre>
[self.tableView registerNib:nib forCellReuseIdentifier:@"CustomCell"];
</pre>

tableView:cellForRowAtIndexPath:
<pre>
CustomCell *cell = [tableView dequeueReusableCellWithIdentifier:@"CustomCell"];
</pre>

5. Set contents to cell as usual. I made NSMutableArray named items in this case.
6. Buid and Run. That's all. It's very easy way!

Author
------

* [@morizotter](http://morizotter.com)
* [Naoki Morita](http://facebook.com/morizotter/)