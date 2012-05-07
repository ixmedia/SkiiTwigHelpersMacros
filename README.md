# SkiiTwigHelpersMacros

List of useful [Twig](http://twig.sensiolabs.org) [Macros](http://twig.sensiolabs.org/doc/tags/macro.html) helpers

## Installation

To use with [Symfony](http://symfony.com) 2.0.x add this in your `deps` file:

	[SkiiTwigHelpersMacros]
		git=http://github.com/ixmedia/SkiiTwigHelpersMacros.git
		target=bundles/Skii/Bundle/TwigHelpersMacrosBundle

Be sure to have it loaded in your Symfony `App/AppKernel.php` file like this:

	class AppKernel extends Kernel
	{
		public function registerBundles()
		{
			$bundles = array(
				…
				new Skii\Bundle\TwigHelpersMacrosBundle\SkiiTwigHelpersMacrosBundle(),
			);
			return $bundles;
		}
		…
	}

## Usage

### Import in your template

And just [import](http://twig.sensiolabs.org/doc/tags/import.html) it in your Twig template as needed:

	{% import 'SkiiTwigHelpersMacrosBundle::helpers.html.twig' as skiiHelpers %}

### Call any helpers where you need it

For example in a Twig template adding this:

	{{ skiiHelpers.tw_follow_btn('iXmedia') }}

Will output something like that:

[![Follow iXmedia](http://f.cl.ly/items/3O3k2c1a393a0d3E2U0U/follow-ixmedia.png)](https://twitter.com/intent/follow?original_referer=http%3A%2F%2Fplatform.twitter.com%2Fwidgets%2Ffollow_button.1335513764.html&region=follow_link&screen_name=iXmedia&source=followbutton&variant=2.0)

## TODO

* Add every type of [Twitter feeds widget](http://twitter.com/about/resources/widgets) support. (Search, List, Faves)

## License

© 2012 [iXmédia](http://www.ixmedia.com) and licensed under the [MIT license](https://github.com/ixmedia/SkiiTwigHelpersMacros/blob/master/LICENSE).