** from a post by WPBeginner that can be found <a href="https://www.wpbeginner.com/wp-themes/how-to-create-a-mobile-ready-responsive-wordpress-menu/" >here</a>

Another common technique to add a mobile menu is by using a slide-in panel menu (as shown in Responsive with toggle effect).

This method requires you to add code to your WordPress theme files, and it is just a different way of accomplishing the same results.

First, you need to open a plain text editor like Notepad and add the following code to a blank text file.

Don’t forget to replace example.com with your own domain name and your-theme with your actual theme directory. Save this file as slidepanel.js to your desktop.

Now you will need an image which will be used as a menu icon. A hamburger icon is most commonly used as the menu icon. You will find tons of such images from different websites. We will be using the menu icon from Google Material Icons library.

Once you find an image that you want to use, save it as menu.png.

Next, you need to open a FTP client client and upload slidepanel.js file to /wp-content/your-theme/js/ folder.

If your theme directory does not have the JS folder, then you need to create tit and then upload your file.

After that, you need to upload menu.png file to /wp-content/themes/your-theme/images/ folder.

Once the files are uploaded, we need to make sure that your theme loads the JavaScript file you just added. We will achieve this by enqueuing the JavaScript file.

Add this code to your theme’s functions.php file.

Now we need to add the actual code in your theme’s header.php file to display the navigation menu. You should look for code similar to this:

You want to wrap existing navigation menu with the HTML code to display your slide panel menu on smaller screens.

Notice that your theme’s navigation menu is still there. We have just wrapped it around HTML that we need to trigger slidepanel menu.

Last step is to add CSS to hide the menu image icon on larger screens. You will also need to adjust the position of the menu icon.

The sample CSS provided is just a starting point. Depending on your WordPress theme, you may need to adjust the CSS to avoid conflicts.