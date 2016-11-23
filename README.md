# Cooldatagridview - Improve the designer of your datagridview.
##### DatagridView BEFORE use the cooldatagridview

[![1.png](https://s15.postimg.org/irxdzqtln/image.png)](https://postimg.org/image/amfc1l5cn/)

##### DatagridView AFTER use the cooldatagridview

[![2.png](https://s15.postimg.org/5z99zthzv/image.png)](https://postimg.org/image/ufrfuaiqf/)

### How to use
 In your Package Manager Console type 
```
  Install-Package cooldatagridview
```
### Exemple
```
dataGridView1.DataSource = database.Product.ToList();
dataGridView1.CoolGrid();
```

### Another functionality
cooldatagridview also allows the user to navigate the arrow keys on the lines of datagridview.

Overwrite the ProcessCmdKey method of the form and place the following code
```
protected override bool ProcessCmdKey(ref Message msg, Keys keyData) {
       
  switch(keyData)
  {
    case: Keys.Up:
	  dataGridView1.MoveToUp();
	  break;
    case: Keys.Down
	  dataGridView1.MoveToDown();
	  break;
    default:
	  break;
  }
  return base.ProcessCmdKey(ref msg, keyData);
}
```

### One more
If you want to hide a column of datagridview you can use

[![5.png](https://s15.postimg.org/tmeu1ocpn/image.png)](https://postimg.org/image/6ky8vxd1z/)
<hr>
### License

It is available under the MIT license.
[License](https://opensource.org/licenses/mit-license.php)



