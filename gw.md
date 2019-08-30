
## The workFlow for Accounts-Sample (page-cli)
>Our template job is focus on **Linux system**, and the following steps are the workflow I test in need.

### **Step 1 :**

I executed this command in the beginning,

`$ npm install -g @motebus/page-cli@latest`

But there is an error happened:

<font color=red >`$ [Error: EACCES: permission denied, access '/usr/local/lib/node_modules- /@motebus /page-cli']`</font>

So I changed the command:

 `$`<font color=#008000 >`sudo`</font>` npm install -g @motebus/page-cli@latest.`

And it works.

### **Step 2 :**

The command below not works,

`$ page init accounts-sample my-project`

<font color=#FF0000 >`Error: EACCES: permission denied, unlink '/home/kiosk/.motebus/accounts-sample/README.md'`
</font>

So I add the command of ‘ sudo’ :

`$`<font color=#008000 >`sudo`</font>` page init accounts-sample my-project`

And it works.

### **Step 3 :**

A new problem happened,

![w.jpg (1258Ã—823)](http://ids.aiot01.com/k.jpg)

I have to change the mode:

`$`<font color=#008000 >`sudo`</font>` chmod –R 777 my-project`

### **Step 4 :**

`cd my-project`

### **Step 5 :**

`$ npm install`

The WARN came out,

<font color=#FF0000 >[‘found 64 vulnerabilities (63 low, 1 critical) run npm audit fix to fix them, or npm audit for details’]</font

But it seems like they wouldn't effect the result.

### **Step 6 :**

Change urls in both store.js and router.js.

### **Step 7 :**

`$ npm run serve`

At the first time, I suffered from this situation.

![w.jpg (1258Ã—823)](http://ids.aiot01.com/w.jpg)

I executed `ctrl+c` and re-command `$ npm run serve` again, and it works perfectly.

