The number of logos is determined in the HTML file. 

Search for this comment:

<!-- Below is the mark-up for the logos -->

Each logo is represented by the following section of code:

  	<li class="logo-icon">
                        <a class="logo-link tempo-link" href="#" target="_blank"> <img class="logo-img tempo-img" alt="tempo logo" src="img/tempo-logo.jpg"></a>
        </li>

To determine whether a logo needs a left border you need to search for this comment in the CSS file:

/* This is where the left border for each logo is fixed */

By default a logo has a left border and is set, thus:

	ul.footer-bottom-logos-icons li {
		border-left: 1px solid #00225A;
	}  

To take away the left border from the logo you need to stipulate which logo you want the border to be removed from by counting from left to right, starting at 1.

Thus, if you want to remove the left border from the 5th logo this is the code you need to use:

	ul.footer-bottom-logos-icons li:nth-child(5) {
  		border-left: 0px solid #00225A;
	} 

Notice that the 5th logo is targeted specifically using:

li:nth-child(5)

You can see this in the actual code supplied!

For each border you want removed you have to include a section of code for each.

Another instance of this can be seen under:

/* ====================== */
/* === 320 WIDTH === */
/* ====================== */

By default each logo is set with a left border, but I don’t want a border for the 1st, 4th and 7th logos. So I write the code like this:

	ul.footer-bottom-logos-icons li {
  		border-left: 1px solid #00225A !Important;
	}  

	ul.footer-bottom-logos-icons li:nth-child(1) {
  		border-left: 0px solid #00225A !Important;
	}  

	ul.footer-bottom-logos-icons li:nth-child(4) {
  		border-left: 0px solid #00225A !Important;
	} 

	ul.footer-bottom-logos-icons li:nth-child(7) {
  		border-left: 0px solid #00225A !Important;
	} 





