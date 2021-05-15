# Test<style>

	.confbox

		{

				visibility:hidden;

						width:300px;height:300px;

								z-index:999;

										position:absolute;

												display:block;

														top:30%;

																left:30%; //adjust the top and left values in the js to better position the box

																	}

																	</style>

<div id="myConfirmBoxName" class="confbox"><h3></h3><p></p><span></span></div>

<a href="#" önclick="myConfirmbox.open();">delete this article</a>

var confirmBox = function(_id)

{

	this.id = _id;

		this.title = 'My dialog';

			this.text = 'Set this value to set the body text';

				this.options = new Array();

					this.domElement = document.getElementById(_id);

						this.visible = false;

	this.addOption = function(txt,val)

		{

				var o = [txt,val];

						options.push(o);

							}

	this.setContent = function(title,body)

		{

				this.domElement.getElementsByTagName('h3')[0].innerHTML = title;

						this.domElement.getElementsByTagName('p')[0].innerHTML = body;

								this.domElement.getElementsByTagName('span')[0].innerHTML = '';/delete/article/321/

										this.domElement.getElementsByTagName('h3')[0].innerHTML = title;

												this.domElement.getElementsByTagName('p')[0].innerHTML = body;

														this.domElement.getElementsByTagName('span')[0].innerHTML = '';

																for (var i=2; i<options.length();i++;)

																		{

																					txt = options[i][0]; //text to show

																								val = options[i][1]; //action to perform. how you handle / process this depends how complex you want to get! callbacks etc... it's up to you.

																											link = '<a href="'+val+'" önclick="document.getElementById(\'+this.id+\'">'+txt+'</a>';

																														this.domElement.getElementsByTagName('span')[0].innerHTML += link;

																																}

																																	}

																																		this.open = function(destination)

																																			{

																																					this.setContent();

																																							if (this.visible)

																																									{

																																												//Add a function here to UNlock the underlying webpage

																																															//Add a function here to center the box

																																																		this.domElement.style.visibility = "visible";

																																																					} else {

																																																									//Add a function here to LOCK the underlying webpage

																																																													this.domElement.style.visibility = "hidden";

																																																																}

																																																																			visible = !visible;

																																																																					}

																																																																						}

																																																																						}

/*and when you are ready to attach the script to the confirm box, ex. after DOM load event or similar, call this:*/

var myConfirmBox = new confirmBox('myConfirmBoxName');

myConfirmbox.title = 'the title i want to use';

myConfirmbox.text = 'the text body I want to show';

myConfirmbox.addOption('Yes',"www.codeproject.com"); 

myConfirmbox.addOption('No',"www.facebook.com");
