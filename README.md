Unlike All Facebook Pages

1. Go to: https://www.facebook.com/usrID/allactivity?activity_history=false&category_key=LIKEDINTERESTS&manage_mode=false&should_load_landing_page=false
2. Paste the following script into console (F12 -> console):
<code>
  var unlike_all = ()=> {
	[].slice.call(document.querySelectorAll('[aria-label="Action options"')).map(x=>{x.click()});
	[].slice.call(document.querySelectorAll('[role="menuitem"')).filter(x=>x.innerText.indexOf('Unlike') !=-1).map(x=>{x.click()});
	window.scrollTo(0,document.body.scrollHeight);
	window.setTimeout(unlike_all, 3 * 1000)
	
};
unlike_all();
</code>
