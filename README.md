CustomCellWithXib
=================

This is an easy way to make CustomCell with Xib.

How to use custom cell with xib file easily.
---------------------------------------------

1. Create a custom UITableViewCell Class. I named it CustomCell.
2. Create xib file for the custom UITableViewCell. I named it CustomCell.xib
3. Customize xib file like placing UILabels or something. And link them to UITableViewCell subclass - in this case, CustomCell.
4. Write two lines below to make UITableView handle CustomCell's instance.
5. Set contents to cell as usual. I made NSMutableArray named it items in this case.
6. Buid and run. That's all. It's very easy way!

**Code**

_viewDidLoad_
<pre>
[self.tableView registerNib:nib forCellReuseIdentifier:@"CustomCell"];
</pre>

_tableView:cellForRowAtIndexPath:_
<pre>
CustomCell *cell = [tableView dequeueReusableCellWithIdentifier:@"CustomCell"];
</pre>

* (Option) I set tableView's height from CustomCell's instance like this.

<pre>
UINib *nib = [UINib nibWithNibName:@"CustomCell" bundle:nil];  
CustomCell *cell = [[nib instantiateWithOwner:nil options:nil]   objectAtIndex:0];
self.tableView.rowHeight = cell.frame.size.height;
</pre>
 


Author
------

* [@morizotter](http://morizotter.com)
* [Naoki Morita](http://facebook.com/morizotter/)