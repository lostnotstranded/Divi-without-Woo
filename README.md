# Divi-without-Woo
A custom Divi stylesheet but without the WooCommerce styles. Useful for those who don't use WooCommerce.

# Don't load what you don't use
Divi, despite being the most popular WordPress theme in the world, does this funny thing where it loads the entirety of its woocommerce on every single page, even on pages that aren't woo or don't use the shop module.

Even worse, it's all concatenated into one file with the rest of the Divi styles, so you can't even dequeue it with PHP.

So instead, I compiled a custom stylesheet for the Divi theme that excludes the WooCommerce styling all together. You're welcome ;)

# How to use this
Always, always, always use a child theme. Just do it. It's just an overall good idea in general to do so. Just do it.

function custom_enqueue() {
  wp_enqueue_style( 'wooless-Divi', get_stylesheet_directory_uri() . '/filename.css' );
}
add_action( 'wp_enqueue_scripts', 'wooless-divi' );

Just upload the file to the main child theme folder and call it whatever you want, and update the "filename.css" in the PHP code I provided.

# Why mess with Divi's stylesheet???
Because that's what I do lol. Divi is great but it's got some shortcoming, shortcomings I solve with code. 
