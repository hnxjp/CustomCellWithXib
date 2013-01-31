CustomCellWithXib
=================

This is an easy way to make CustomCell with Xib.

How to use custom cell with xib file easily.
---------------------------------------------

1. Create Custom UITableViewCell Class. I named it CustomCell.
2. Create Xib file for Custom UITableViewCell. I named it CustomCell.xib
3. Customize xib file like putting UILabels or something. And link them to UITableViewCell subclass - In this case, CustomCell.
4. Write two lines below to make UITableView handle CustomCell's instance.

<pre>
[self.tableView registerNib:nib forCellReuseIdentifier:@"CustomCell"];
</pre>
<pre>
CustomCell *cell = [tableView dequeueReusableCellWithIdentifier:@"CustomCell"];
</pre>

5. Set contents to cell as usual. I made NSMutableArray named items in this case.
6. Buid and Run. That's all. It's very easy way!

Author
------

* [@morizotter](http://morizotter.com)
* [Naoki Morita](http://facebook.com/morizotter/)