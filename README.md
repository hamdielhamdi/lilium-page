<html lang="en-US"><head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>$HOSKY Token</title>
<meta name="robots" content="max-image-preview:large">
<link rel="dns-prefetch" href="//hosky.io">
<link rel="dns-prefetch" href="//s.w.org">
<link rel="alternate" type="application/rss+xml" title="$HOSKY Token » Feed" href="https://hosky.io/feed/">
<link rel="alternate" type="application/rss+xml" title="$HOSKY Token » Comments Feed" href="https://hosky.io/comments/feed/">
		<!-- This site uses the Google Analytics by MonsterInsights plugin v8.3.0 - Using Analytics tracking - https://www.monsterinsights.com/ -->
							<script src="//www.googletagmanager.com/gtag/js?id=G-9SCYESR2J2" type="text/javascript" data-cfasync="false" data-wpfc-render="false" async=""></script>
			<script type="text/javascript" data-cfasync="false" data-wpfc-render="false">
				var mi_version = '8.3.0';
				var mi_track_user = true;
				var mi_no_track_reason = '';
				
								var disableStrs = [
										'ga-disable-G-9SCYESR2J2',
														];

				/* Function to detect opted out users */
				function __gtagTrackerIsOptedOut() {
					for ( var index = 0; index < disableStrs.length; index++ ) {
						if ( document.cookie.indexOf( disableStrs[ index ] + '=true' ) > -1 ) {
							return true;
						}
					}

					return false;
				}

				/* Disable tracking if the opt-out cookie exists. */
				if ( __gtagTrackerIsOptedOut() ) {
					for ( var index = 0; index < disableStrs.length; index++ ) {
						window[ disableStrs[ index ] ] = true;
					}
				}

				/* Opt-out function */
				function __gtagTrackerOptout() {
					for ( var index = 0; index < disableStrs.length; index++ ) {
						document.cookie = disableStrs[ index ] + '=true; expires=Thu, 31 Dec 2099 23:59:59 UTC; path=/';
						window[ disableStrs[ index ] ] = true;
					}
				}

				if ( 'undefined' === typeof gaOptout ) {
					function gaOptout() {
						__gtagTrackerOptout();
					}
				}
								window.dataLayer = window.dataLayer || [];

				window.MonsterInsightsDualTracker = {
					helpers: {},
					trackers: {},
				};
				if ( mi_track_user ) {
					function __gtagDataLayer() {
						dataLayer.push( arguments );
					}

					function __gtagTracker( type, name, parameters ) {
						if (!parameters) {
							parameters = {};
						}

						if (parameters.send_to) {
							__gtagDataLayer.apply( null, arguments );
							return;
						}

						if ( type === 'event' ) {
															parameters.send_to = monsterinsights_frontend.v4_id;
								var hookName = name;
								if ( typeof parameters[ 'event_category' ] !== 'undefined' ) {
									hookName = parameters[ 'event_category' ] + ':' + name;
								}

								if ( typeof MonsterInsightsDualTracker.trackers[ hookName ] !== 'undefined' ) {
									MonsterInsightsDualTracker.trackers[ hookName ]( parameters );
								} else {
									__gtagDataLayer( 'event', name, parameters );
								}
							
													} else {
							__gtagDataLayer.apply( null, arguments );
						}
					}
					__gtagTracker( 'js', new Date() );
					__gtagTracker( 'set', {
						'developer_id.dZGIzZG' : true,
											} );
										__gtagTracker( 'config', 'G-9SCYESR2J2', {"forceSSL":"true","link_attribution":"true"} );
															window.gtag = __gtagTracker;											(function () {
							/* https://developers.google.com/analytics/devguides/collection/analyticsjs/ */
							/* ga and __gaTracker compatibility shim. */
							var noopfn = function () {
								return null;
							};
							var newtracker = function () {
								return new Tracker();
							};
							var Tracker = function () {
								return null;
							};
							var p = Tracker.prototype;
							p.get = noopfn;
							p.set = noopfn;
							p.send = function (){
								var args = Array.prototype.slice.call(arguments);
								args.unshift( 'send' );
								__gaTracker.apply(null, args);
							};
							var __gaTracker = function () {
								var len = arguments.length;
								if ( len === 0 ) {
									return;
								}
								var f = arguments[len - 1];
								if ( typeof f !== 'object' || f === null || typeof f.hitCallback !== 'function' ) {
									if ( 'send' === arguments[0] ) {
										var hitConverted, hitObject = false, action;
										if ( 'event' === arguments[1] ) {
											if ( 'undefined' !== typeof arguments[3] ) {
												hitObject = {
													'eventAction': arguments[3],
													'eventCategory': arguments[2],
													'eventLabel': arguments[4],
													'value': arguments[5] ? arguments[5] : 1,
												}
											}
										}
										if ( 'pageview' === arguments[1] ) {
											if ( 'undefined' !== typeof arguments[2] ) {
												hitObject = {
													'eventAction': 'page_view',
													'page_path' : arguments[2],
												}
											}
										}
										if ( typeof arguments[2] === 'object' ) {
											hitObject = arguments[2];
										}
										if ( typeof arguments[5] === 'object' ) {
											Object.assign( hitObject, arguments[5] );
										}
										if ( 'undefined' !== typeof arguments[1].hitType ) {
											hitObject = arguments[1];
											if ( 'pageview' === hitObject.hitType ) {
												hitObject.eventAction = 'page_view';
											}
										}
										if ( hitObject ) {
											action = 'timing' === arguments[1].hitType ? 'timing_complete' : hitObject.eventAction;
											hitConverted = mapArgs( hitObject );
											__gtagTracker( 'event', action, hitConverted );
										}
									}
									return;
								}

								function mapArgs( args ) {
									var arg, hit = {};
									var gaMap = {
										'eventCategory': 'event_category',
										'eventAction': 'event_action',
										'eventLabel': 'event_label',
										'eventValue': 'event_value',
										'nonInteraction': 'non_interaction',
										'timingCategory': 'event_category',
										'timingVar': 'name',
										'timingValue': 'value',
										'timingLabel': 'event_label',
										'page' : 'page_path',
										'location' : 'page_location',
										'title' : 'page_title',
									};
									for ( arg in args ) {
																				if ( ! ( ! args.hasOwnProperty(arg) || ! gaMap.hasOwnProperty(arg) ) ) {
											hit[gaMap[arg]] = args[arg];
										} else {
											hit[arg] = args[arg];
										}
									}
									return hit;
								}

								try {
									f.hitCallback();
								} catch ( ex ) {
								}
							};
							__gaTracker.create = newtracker;
							__gaTracker.getByName = newtracker;
							__gaTracker.getAll = function () {
								return [];
							};
							__gaTracker.remove = noopfn;
							__gaTracker.loaded = true;
							window['__gaTracker'] = __gaTracker;
						})();
									} else {
										console.log( "" );
					( function () {
							function __gtagTracker() {
								return null;
							}
							window['__gtagTracker'] = __gtagTracker;
							window['gtag'] = __gtagTracker;
					} )();
									}
			</script>
				<!-- / Google Analytics by MonsterInsights -->
				<script>
			window._wpemojiSettings = {"baseUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.1.0\/72x72\/","ext":".png","svgUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.1.0\/svg\/","svgExt":".svg","source":{"concatemoji":"https:\/\/hosky.io\/wp-includes\/js\/wp-emoji-release.min.js?ver=5.8.3"}};
			!function(e,a,t){var n,r,o,i=a.createElement("canvas"),p=i.getContext&&i.getContext("2d");function s(e,t){var a=String.fromCharCode;p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,e),0,0);e=i.toDataURL();return p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,t),0,0),e===i.toDataURL()}function c(e){var t=a.createElement("script");t.src=e,t.defer=t.type="text/javascript",a.getElementsByTagName("head")[0].appendChild(t)}for(o=Array("flag","emoji"),t.supports={everything:!0,everythingExceptFlag:!0},r=0;r<o.length;r++)t.supports[o[r]]=function(e){if(!p||!p.fillText)return!1;switch(p.textBaseline="top",p.font="600 32px Arial",e){case"flag":return s([127987,65039,8205,9895,65039],[127987,65039,8203,9895,65039])?!1:!s([55356,56826,55356,56819],[55356,56826,8203,55356,56819])&&!s([55356,57332,56128,56423,56128,56418,56128,56421,56128,56430,56128,56423,56128,56447],[55356,57332,8203,56128,56423,8203,56128,56418,8203,56128,56421,8203,56128,56430,8203,56128,56423,8203,56128,56447]);case"emoji":return!s([10084,65039,8205,55357,56613],[10084,65039,8203,55357,56613])}return!1}(o[r]),t.supports.everything=t.supports.everything&&t.supports[o[r]],"flag"!==o[r]&&(t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&t.supports[o[r]]);t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&!t.supports.flag,t.DOMReady=!1,t.readyCallback=function(){t.DOMReady=!0},t.supports.everything||(n=function(){t.readyCallback()},a.addEventListener?(a.addEventListener("DOMContentLoaded",n,!1),e.addEventListener("load",n,!1)):(e.attachEvent("onload",n),a.attachEvent("onreadystatechange",function(){"complete"===a.readyState&&t.readyCallback()})),(n=t.source||{}).concatemoji?c(n.concatemoji):n.wpemoji&&n.twemoji&&(c(n.twemoji),c(n.wpemoji)))}(window,document,window._wpemojiSettings);
		</script><script src="https://hosky.io/wp-includes/js/wp-emoji-release.min.js?ver=5.8.3" type="text/javascript" defer=""></script>
		<style>
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 .07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
	<link rel="stylesheet" id="wp-block-library-css" href="https://hosky.io/wp-includes/css/dist/block-library/style.min.css?ver=5.8.3" media="all">
<style id="wp-block-library-theme-inline-css">
#start-resizable-editor-section{display:none}.wp-block-audio figcaption{color:#555;font-size:13px;text-align:center}.is-dark-theme .wp-block-audio figcaption{color:hsla(0,0%,100%,.65)}.wp-block-code{font-family:Menlo,Consolas,monaco,monospace;color:#1e1e1e;padding:.8em 1em;border:1px solid #ddd;border-radius:4px}.wp-block-embed figcaption{color:#555;font-size:13px;text-align:center}.is-dark-theme .wp-block-embed figcaption{color:hsla(0,0%,100%,.65)}.blocks-gallery-caption{color:#555;font-size:13px;text-align:center}.is-dark-theme .blocks-gallery-caption{color:hsla(0,0%,100%,.65)}.wp-block-image figcaption{color:#555;font-size:13px;text-align:center}.is-dark-theme .wp-block-image figcaption{color:hsla(0,0%,100%,.65)}.wp-block-pullquote{border-top:4px solid;border-bottom:4px solid;margin-bottom:1.75em;color:currentColor}.wp-block-pullquote__citation,.wp-block-pullquote cite,.wp-block-pullquote footer{color:currentColor;text-transform:uppercase;font-size:.8125em;font-style:normal}.wp-block-quote{border-left:.25em solid;margin:0 0 1.75em;padding-left:1em}.wp-block-quote cite,.wp-block-quote footer{color:currentColor;font-size:.8125em;position:relative;font-style:normal}.wp-block-quote.has-text-align-right{border-left:none;border-right:.25em solid;padding-left:0;padding-right:1em}.wp-block-quote.has-text-align-center{border:none;padding-left:0}.wp-block-quote.is-large,.wp-block-quote.is-style-large{border:none}.wp-block-search .wp-block-search__label{font-weight:700}.wp-block-group.has-background{padding:1.25em 2.375em;margin-top:0;margin-bottom:0}.wp-block-separator{border:none;border-bottom:2px solid;margin-left:auto;margin-right:auto;opacity:.4}.wp-block-separator:not(.is-style-wide):not(.is-style-dots){width:100px}.wp-block-separator.has-background:not(.is-style-dots){border-bottom:none;height:1px}.wp-block-separator.has-background:not(.is-style-wide):not(.is-style-dots){height:2px}.wp-block-table thead{border-bottom:3px solid}.wp-block-table tfoot{border-top:3px solid}.wp-block-table td,.wp-block-table th{padding:.5em;border:1px solid;word-break:normal}.wp-block-table figcaption{color:#555;font-size:13px;text-align:center}.is-dark-theme .wp-block-table figcaption{color:hsla(0,0%,100%,.65)}.wp-block-video figcaption{color:#555;font-size:13px;text-align:center}.is-dark-theme .wp-block-video figcaption{color:hsla(0,0%,100%,.65)}.wp-block-template-part.has-background{padding:1.25em 2.375em;margin-top:0;margin-bottom:0}#end-resizable-editor-section{display:none}
</style>
<link rel="stylesheet" id="twenty-twenty-one-style-css" href="https://hosky.io/wp-content/themes/twentytwentyone/style.css?ver=1.4" media="all">
<style id="twenty-twenty-one-style-inline-css">
:root{--global--color-background: #206cd2;--global--color-primary: #fff;--global--color-secondary: #fff;--button--color-background: #fff;--button--color-text-hover: #fff;--table--stripes-border-color: rgba(240, 240, 240, 0.15);--table--stripes-background-color: rgba(240, 240, 240, 0.15);}
@supports (-webkit-appearance: none) or (-moz-appearance: none) {
				div.wpforms-container-full .wpforms-form input[type=checkbox] {
					-webkit-appearance: checkbox;
					-moz-appearance: checkbox;
				}
				div.wpforms-container-full .wpforms-form input[type=radio] {
					-webkit-appearance: radio;
					-moz-appearance: radio;
				}
				div.wpforms-container-full .wpforms-form input[type=checkbox]:after,
				div.wpforms-container-full .wpforms-form input[type=radio]:after {
					content: none;
				}
			}
div.wpforms-container-full form.wpforms-form select {
				background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='10' height='10' fill='%2328303d'><polygon points='0,0 10,0 5,5'/></svg>");
				background-repeat: no-repeat;
				background-position: right var(--form--spacing-unit) top 60%;
			}
</style>
<link rel="stylesheet" id="twenty-twenty-one-print-style-css" href="https://hosky.io/wp-content/themes/twentytwentyone/assets/css/print.css?ver=1.4" media="print">
<link rel="stylesheet" id="popup-maker-site-css" href="//hosky.io/wp-content/uploads/pum/pum-site-styles.css?generated=1639962930&amp;ver=1.16.2" media="all">
<script id="monsterinsights-frontend-script-js-extra">
var monsterinsights_frontend = {"js_events_tracking":"true","download_extensions":"doc,pdf,ppt,zip,xls,docx,pptx,xlsx","inbound_paths":"[{\"path\":\"\\\/go\\\/\",\"label\":\"affiliate\"},{\"path\":\"\\\/recommend\\\/\",\"label\":\"affiliate\"}]","home_url":"https:\/\/hosky.io","hash_tracking":"false","ua":"","v4_id":"G-9SCYESR2J2"};
</script>
<script src="https://hosky.io/wp-content/plugins/google-analytics-for-wordpress/assets/js/frontend-gtag.min.js?ver=8.3.0" id="monsterinsights-frontend-script-js"></script>
<script src="https://hosky.io/wp-includes/js/jquery/jquery.min.js?ver=3.6.0" id="jquery-core-js"></script>
<script src="https://hosky.io/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2" id="jquery-migrate-js"></script>
<link rel="https://api.w.org/" href="https://hosky.io/wp-json/"><link rel="alternate" type="application/json" href="https://hosky.io/wp-json/wp/v2/pages/10"><link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://hosky.io/xmlrpc.php?rsd">
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://hosky.io/wp-includes/wlwmanifest.xml"> 
<meta name="generator" content="WordPress 5.8.3">
<link rel="canonical" href="https://hosky.io/">
<link rel="shortlink" href="https://hosky.io/">
<link rel="alternate" type="application/json+oembed" href="https://hosky.io/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fhosky.io%2F">
<link rel="alternate" type="text/xml+oembed" href="https://hosky.io/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fhosky.io%2F&amp;format=xml">
<!--Customizer CSS--> 
<style type="text/css">
.powered-by {
    display: none;
}
</style> 
<!--/Customizer CSS-->
<style id="custom-background-css">
body.custom-background { background-color: #206cd2; }
</style>
			<style id="wp-custom-css">
			.site-header { display:none}
.site-info { display: none}
		</style>
		</head>

<body class="home page-template-default page page-id-10 custom-background wp-embed-responsive is-dark-theme singular has-main-navigation no-widgets">
<div id="page" class="site">
	<a class="skip-link screen-reader-text" href="#content">Skip to content</a>

	
<header id="masthead" class="site-header has-menu" role="banner">

	

<div class="site-branding">

	
						<h1 class="screen-reader-text">$HOSKY Token</h1>
			
	</div><!-- .site-branding -->
	
	<nav id="site-navigation" class="primary-navigation" role="navigation" aria-label="Primary menu">
		<div class="menu-button-container">
			<button id="primary-mobile-menu" class="button" aria-controls="primary-menu-list" aria-expanded="false">
				<span class="dropdown-icon open">Menu					<svg class="svg-icon" width="24" height="24" aria-hidden="true" role="img" focusable="false" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M4.5 6H19.5V7.5H4.5V6ZM4.5 12H19.5V13.5H4.5V12ZM19.5 18H4.5V19.5H19.5V18Z" fill="currentColor"></path></svg>				</span>
				<span class="dropdown-icon close">Close					<svg class="svg-icon" width="24" height="24" aria-hidden="true" role="img" focusable="false" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M12 10.9394L5.53033 4.46973L4.46967 5.53039L10.9393 12.0001L4.46967 18.4697L5.53033 19.5304L12 13.0607L18.4697 19.5304L19.5303 18.4697L13.0607 12.0001L19.5303 5.53039L18.4697 4.46973L12 10.9394Z" fill="currentColor"></path></svg>				</span>
			</button><!-- #primary-mobile-menu -->
		</div><!-- .menu-button-container -->
		<div class="primary-menu-container"><ul id="primary-menu-list" class="menu-wrapper"><li id="menu-item-20" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20"><a href="https://discord.gg/C2JFwAdRru">Discord</a></li>
<li id="menu-item-21" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-21"><a href="https://t.me/joinchat/yGcJxytvsSJmZDAx%20https://t.me/joinchat/yGcJxytvsSJmZDAx">Telegram</a></li>
<li id="menu-item-22" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-22"><a href="https://twitter.com/hoskytoken">Twitter</a></li>
</ul></div>	</nav><!-- #site-navigation -->

</header><!-- #masthead -->

	<div id="content" class="site-content">
		<div id="primary" class="content-area">
			<main id="main" class="site-main" role="main">

<article id="post-10" class="post-10 page type-page status-publish hentry entry">

	
	<div class="entry-content">
		
<ul class="wp-block-social-links aligncenter has-large-icon-size has-icon-color items-justified-center is-style-twentytwentyone-social-icons-color"><li style="color: #FFFFFF; " class="wp-social-link wp-social-link-twitter wp-block-social-link"><a href="https://twitter.com/hoskytoken" aria-label="Twitter: https://twitter.com/hoskytoken" rel="noopener nofollow" target="_blank" class="wp-block-social-link-anchor"> <svg width="24" height="24" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" role="img" aria-hidden="true" focusable="false"><path d="M22.23,5.924c-0.736,0.326-1.527,0.547-2.357,0.646c0.847-0.508,1.498-1.312,1.804-2.27 c-0.793,0.47-1.671,0.812-2.606,0.996C18.324,4.498,17.257,4,16.077,4c-2.266,0-4.103,1.837-4.103,4.103 c0,0.322,0.036,0.635,0.106,0.935C8.67,8.867,5.647,7.234,3.623,4.751C3.27,5.357,3.067,6.062,3.067,6.814 c0,1.424,0.724,2.679,1.825,3.415c-0.673-0.021-1.305-0.206-1.859-0.513c0,0.017,0,0.034,0,0.052c0,1.988,1.414,3.647,3.292,4.023 c-0.344,0.094-0.707,0.144-1.081,0.144c-0.264,0-0.521-0.026-0.772-0.074c0.522,1.63,2.038,2.816,3.833,2.85 c-1.404,1.1-3.174,1.756-5.096,1.756c-0.331,0-0.658-0.019-0.979-0.057c1.816,1.164,3.973,1.843,6.29,1.843 c7.547,0,11.675-6.252,11.675-11.675c0-0.178-0.004-0.355-0.012-0.531C20.985,7.47,21.68,6.747,22.23,5.924z"></path></svg></a></li>

<li style="color: #FFFFFF; " class="wp-social-link wp-social-link-telegram wp-block-social-link"><a href="https://t.me/joinchat/yGcJxytvsSJmZDAx%20addr1vxpzmhj8vsu62fs8pumd85tx0tgfndrzcygump0q38670asr4vgg6%20https://t.me/joinchat/yGcJxytvsSJmZDAx" aria-label="Telegram: https://t.me/joinchat/yGcJxytvsSJmZDAx addr1vxpzmhj8vsu62fs8pumd85tx0tgfndrzcygump0q38670asr4vgg6 https://t.me/joinchat/yGcJxytvsSJmZDAx" rel="noopener nofollow" target="_blank" class="wp-block-social-link-anchor"> <svg width="24" height="24" viewBox="0 0 128 128" version="1.1" xmlns="http://www.w3.org/2000/svg" role="img" aria-hidden="true" focusable="false"><path d="M28.9700376,63.3244248 C47.6273373,55.1957357 60.0684594,49.8368063 66.2934036,47.2476366 C84.0668845,39.855031 87.7600616,38.5708563 90.1672227,38.528 C90.6966555,38.5191258 91.8804274,38.6503351 92.6472251,39.2725385 C93.294694,39.7979149 93.4728387,40.5076237 93.5580865,41.0057381 C93.6433345,41.5038525 93.7494885,42.63857 93.6651041,43.5252052 C92.7019529,53.6451182 88.5344133,78.2034783 86.4142057,89.5379542 C85.5170662,94.3339958 83.750571,95.9420841 82.0403991,96.0994568 C78.3237996,96.4414641 75.5015827,93.6432685 71.9018743,91.2836143 C66.2690414,87.5912212 63.0868492,85.2926952 57.6192095,81.6896017 C51.3004058,77.5256038 55.3966232,75.2369981 58.9976911,71.4967761 C59.9401076,70.5179421 76.3155302,55.6232293 76.6324771,54.2720454 C76.6721165,54.1030573 76.7089039,53.4731496 76.3346867,53.1405352 C75.9604695,52.8079208 75.4081573,52.921662 75.0095933,53.0121213 C74.444641,53.1403447 65.4461175,59.0880351 48.0140228,70.8551922 C45.4598218,72.6091037 43.1463059,73.4636682 41.0734751,73.4188859 C38.7883453,73.3695169 34.3926725,72.1268388 31.1249416,71.0646282 C27.1169366,69.7617838 23.931454,69.0729605 24.208838,66.8603276 C24.3533167,65.7078514 25.9403832,64.5292172 28.9700376,63.3244248 Z"></path></svg></a></li>

<li style="color: #FFFFFF; " class="wp-social-link wp-social-link-chain wp-block-social-link"><a href="https://discord.gg/C2JFwAdRru" aria-label="Discord" rel="noopener nofollow" target="_blank" class="wp-block-social-link-anchor"> <svg width="24" height="24" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" role="img" aria-hidden="true" focusable="false"><path d="M19.647,16.706a1.134,1.134,0,0,0-.343-.833l-2.549-2.549a1.134,1.134,0,0,0-.833-.343,1.168,1.168,0,0,0-.883.392l.233.226q.2.189.264.264a2.922,2.922,0,0,1,.184.233.986.986,0,0,1,.159.312,1.242,1.242,0,0,1,.043.337,1.172,1.172,0,0,1-1.176,1.176,1.237,1.237,0,0,1-.337-.043,1,1,0,0,1-.312-.159,2.76,2.76,0,0,1-.233-.184q-.073-.068-.264-.264l-.226-.233a1.19,1.19,0,0,0-.4.895,1.134,1.134,0,0,0,.343.833L15.837,19.3a1.13,1.13,0,0,0,.833.331,1.18,1.18,0,0,0,.833-.318l1.8-1.789a1.12,1.12,0,0,0,.343-.821Zm-8.615-8.64a1.134,1.134,0,0,0-.343-.833L8.163,4.7a1.134,1.134,0,0,0-.833-.343,1.184,1.184,0,0,0-.833.331L4.7,6.473a1.12,1.12,0,0,0-.343.821,1.134,1.134,0,0,0,.343.833l2.549,2.549a1.13,1.13,0,0,0,.833.331,1.184,1.184,0,0,0,.883-.38L8.728,10.4q-.2-.189-.264-.264A2.922,2.922,0,0,1,8.28,9.9a.986.986,0,0,1-.159-.312,1.242,1.242,0,0,1-.043-.337A1.172,1.172,0,0,1,9.254,8.079a1.237,1.237,0,0,1,.337.043,1,1,0,0,1,.312.159,2.761,2.761,0,0,1,.233.184q.073.068.264.264l.226.233a1.19,1.19,0,0,0,.4-.895ZM22,16.706a3.343,3.343,0,0,1-1.042,2.488l-1.8,1.789a3.536,3.536,0,0,1-4.988-.025l-2.525-2.537a3.384,3.384,0,0,1-1.017-2.488,3.448,3.448,0,0,1,1.078-2.561l-1.078-1.078a3.434,3.434,0,0,1-2.549,1.078,3.4,3.4,0,0,1-2.5-1.029L3.029,9.794A3.4,3.4,0,0,1,2,7.294,3.343,3.343,0,0,1,3.042,4.806l1.8-1.789A3.384,3.384,0,0,1,7.331,2a3.357,3.357,0,0,1,2.5,1.042l2.525,2.537a3.384,3.384,0,0,1,1.017,2.488,3.448,3.448,0,0,1-1.078,2.561l1.078,1.078a3.551,3.551,0,0,1,5.049-.049l2.549,2.549A3.4,3.4,0,0,1,22,16.706Z"></path></svg></a></li></ul>



<div class="wp-block-image is-style-default"><figure class="aligncenter size-large is-resized"><img loading="lazy" src="https://hosky.io/wp-content/uploads/2021/11/Hosky-1-1024x1024.png" alt="" class="wp-image-32" width="512" height="512" srcset="https://hosky.io/wp-content/uploads/2021/11/Hosky-1-1024x1024.png 1024w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-300x300.png 300w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-150x150.png 150w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-768x768.png 768w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-1536x1536.png 1536w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-2048x2048.png 2048w, https://hosky.io/wp-content/uploads/2021/11/Hosky-1-1568x1568.png 1568w" sizes="(max-width: 512px) 100vw, 512px"></figure></div>



<h3 class="has-text-align-center"><meta charset="utf-8"><strong>C(ash grab)NFT</strong></h3>



<div class="wp-block-image is-style-default popmake-206 pum-trigger" style="cursor: pointer;"><figure class="aligncenter size-large"><img loading="lazy" width="1024" height="651" src="https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-1024x651.png" alt="" class="wp-image-188" srcset="https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-1024x651.png 1024w, https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-300x191.png 300w, https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-768x488.png 768w, https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-1536x977.png 1536w, https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-2048x1303.png 2048w, https://hosky.io/wp-content/uploads/2021/11/nft-printer-OG-1568x997.png 1568w" sizes="(max-width: 1024px) 100vw, 1024px"></figure></div>



<div class="wp-block-columns alignwide are-vertically-aligned-top">
<div class="wp-block-column is-vertically-aligned-top">
<h3 class="has-text-align-center"><strong>BROWN PAPER</strong></h3>



<div class="wp-block-image is-style-default"><figure class="aligncenter size-large is-resized"><a href="https://hosky.io/wp-content/uploads/2021/11/Brown-Paw-per-v0.69-Revision-420.pdf"><img loading="lazy" src="https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-843x1024.png" alt="" class="wp-image-96" width="211" height="256" srcset="https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-843x1024.png 843w, https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-247x300.png 247w, https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-768x933.png 768w, https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-1265x1536.png 1265w, https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-1687x2048.png 1687w, https://hosky.io/wp-content/uploads/2021/11/Brown-Paper-1568x1904.png 1568w" sizes="(max-width: 211px) 100vw, 211px"></a></figure></div>
</div>



<div class="wp-block-column is-vertically-aligned-top">
<h3 class="has-text-align-center"><strong>DOGGIE BOWL™</strong></h3>



<div class="wp-block-image is-style-default popmake-63 pum-trigger" style="cursor: pointer;"><figure class="aligncenter size-medium"><img loading="lazy" width="300" height="212" src="https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-300x212.png" alt="" class="wp-image-39" title="popmake-63" srcset="https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-300x212.png 300w, https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-1024x723.png 1024w, https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-768x542.png 768w, https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-1536x1084.png 1536w, https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-2048x1446.png 2048w, https://hosky.io/wp-content/uploads/2021/11/Doggie-Bowl-2-1568x1107.png 1568w" sizes="(max-width: 300px) 100vw, 300px"></figure></div>
</div>
</div>



<p style="font-size:15px">Tokenn Policy ID: a0028f350aaabe0545fdcb56b039bfb08e4bb4d8c4d7c3c7d481c235<br>NFT Policy ID: a5bb0e5bb275a573d744a021f9b3bff73595468e002755b447e01559</p>



<div class="wp-block-image is-style-default popmake-161 pum-trigger" style="cursor: pointer;"><figure class="aligncenter size-large is-resized"><img loading="lazy" src="https://hosky.io/wp-content/uploads/2021/11/Poop-843x1024.png" alt="" class="wp-image-158" width="53" height="64" srcset="https://hosky.io/wp-content/uploads/2021/11/Poop-843x1024.png 843w, https://hosky.io/wp-content/uploads/2021/11/Poop-247x300.png 247w, https://hosky.io/wp-content/uploads/2021/11/Poop-768x933.png 768w, https://hosky.io/wp-content/uploads/2021/11/Poop-1265x1536.png 1265w, https://hosky.io/wp-content/uploads/2021/11/Poop-1687x2048.png 1687w, https://hosky.io/wp-content/uploads/2021/11/Poop-1568x1904.png 1568w" sizes="(max-width: 53px) 100vw, 53px"></figure></div>



<p> </p>
	</div><!-- .entry-content -->

	</article><!-- #post-10 -->
			</main><!-- #main -->
		</div><!-- #primary -->
	</div><!-- #content -->

	
	<footer id="colophon" class="site-footer" role="contentinfo">

				<div class="site-info">
			<div class="site-name">
																</div><!-- .site-name -->
			<div class="powered-by">
				Proudly powered by <a href="https://wordpress.org/">WordPress</a>.			</div><!-- .powered-by -->

		</div><!-- .site-info -->
	</footer><!-- #colophon -->

</div><!-- #page -->

<div id="pum-206" class="pum pum-overlay pum-theme-54 pum-theme-default-theme popmake-overlay click_open" data-popmake="{&quot;id&quot;:206,&quot;slug&quot;:&quot;hosky-cash-grabnft&quot;,&quot;theme_id&quot;:54,&quot;cookies&quot;:[],&quot;triggers&quot;:[{&quot;type&quot;:&quot;click_open&quot;,&quot;settings&quot;:{&quot;cookie_name&quot;:&quot;&quot;,&quot;extra_selectors&quot;:&quot;&quot;}}],&quot;mobile_disabled&quot;:null,&quot;tablet_disabled&quot;:null,&quot;meta&quot;:{&quot;display&quot;:{&quot;stackable&quot;:false,&quot;overlay_disabled&quot;:false,&quot;scrollable_content&quot;:false,&quot;disable_reposition&quot;:false,&quot;size&quot;:&quot;medium&quot;,&quot;responsive_min_width&quot;:&quot;0%&quot;,&quot;responsive_min_width_unit&quot;:false,&quot;responsive_max_width&quot;:&quot;100%&quot;,&quot;responsive_max_width_unit&quot;:false,&quot;custom_width&quot;:&quot;640px&quot;,&quot;custom_width_unit&quot;:false,&quot;custom_height&quot;:&quot;380px&quot;,&quot;custom_height_unit&quot;:false,&quot;custom_height_auto&quot;:false,&quot;location&quot;:&quot;center top&quot;,&quot;position_from_trigger&quot;:false,&quot;position_top&quot;:&quot;100&quot;,&quot;position_left&quot;:&quot;0&quot;,&quot;position_bottom&quot;:&quot;0&quot;,&quot;position_right&quot;:&quot;0&quot;,&quot;position_fixed&quot;:false,&quot;animation_type&quot;:&quot;fade&quot;,&quot;animation_speed&quot;:&quot;350&quot;,&quot;animation_origin&quot;:&quot;center top&quot;,&quot;overlay_zindex&quot;:false,&quot;zindex&quot;:&quot;1999999999&quot;},&quot;close&quot;:{&quot;text&quot;:&quot;&quot;,&quot;button_delay&quot;:&quot;0&quot;,&quot;overlay_click&quot;:false,&quot;esc_press&quot;:false,&quot;f4_press&quot;:false},&quot;click_open&quot;:[]}}" role="dialog" aria-hidden="true" aria-labelledby="pum_popup_title_206">

	<div id="popmake-206" class="pum-container popmake theme-54 pum-responsive pum-responsive-medium responsive size-medium">

				

				            <div id="pum_popup_title_206" class="pum-title popmake-title">
				HOSKY C(ash grab)NFT			</div>
		

		

				<div class="pum-content popmake-content" tabindex="0">
			<p style="text-align: center;"><strong>Before buying our C(ash grab)NFT please read the following:<br>
</strong><span style="font-weight: 400;">1. This is the least exclusive, low-quality, biggest Cash Grab in Cardano History.<br>
</span><span style="font-weight: 400;">2. Understand that this is&nbsp;<strong>not</strong> art, they have&nbsp;<strong>no</strong> utility, they are <strong>just PNGS</strong>.<br>
</span><span style="font-weight: 400;">3. Ensure you are using a </span><span style="font-weight: 400;">Shell-Era wallet </span><span style="font-weight: 400;">that supports native assets.</span><span style="font-weight: 400;"><br>
</span><span style="font-weight: 400;">4. </span><span style="font-weight: 400;">Do </span><b>NOT</b><span style="font-weight: 400;">, we repeat </span><span style="font-weight: 400;">Do</span> <b>NOT</b><span style="font-weight: 400;"> send funds from an exchange, your funds could be lost, and you will not receive your CNFT.<br>
<span style="color: #ff0000;"><strong>THERE WILL BE A 24 HOUR DELAY BEFORE NFTS WILL BEGIN TO BE DELIVERED</strong></span></span></p>
<pre><img loading="lazy" class="size-full wp-image-212 aligncenter" src="https://hosky.io/wp-content/uploads/2021/12/NFT-1.png" alt="" width="200" height="200" srcset="https://hosky.io/wp-content/uploads/2021/12/NFT-1.png 200w, https://hosky.io/wp-content/uploads/2021/12/NFT-1-150x150.png 150w" sizes="(max-width: 200px) 100vw, 200px"></pre>
<p class="p1" style="text-align: center;"><strong>addr1v89w4j93c75dfh99qg5lhzvqx82984gh7r2ylh7pv8zzg4cxs67jj</strong></p>
<p><span style="font-weight: 400;">In order to receive HOSKY C(ash grab)NFT please send the correct amount in increments 6.9 $ADA to the provided address above, when you do, we will then return the corresponding number of NFT’s (see chart below for valid increments)<br>
<img loading="lazy" class="aligncenter wp-image-217 size-medium" src="https://hosky.io/wp-content/uploads/2021/12/NFTPull-300x250.png" alt="" width="300" height="250" srcset="https://hosky.io/wp-content/uploads/2021/12/NFTPull-300x250.png 300w, https://hosky.io/wp-content/uploads/2021/12/NFTPull.png 504w" sizes="(max-width: 300px) 100vw, 300px"><br>
</span></p>
<p><img class="aligncenter"></p>
<p><span style="font-weight: 400;">– Woof!</span></p>
<p>&nbsp;</p>
		</div>


				

				            <button type="button" class="pum-close popmake-close" aria-label="Close">
			CLOSE            </button>
		
	</div>

</div>
<div id="pum-63" class="pum pum-overlay pum-theme-57 pum-theme-hello-box popmake-overlay click_open" data-popmake="{&quot;id&quot;:63,&quot;slug&quot;:&quot;doggie-bowl&quot;,&quot;theme_id&quot;:57,&quot;cookies&quot;:[],&quot;triggers&quot;:[{&quot;type&quot;:&quot;click_open&quot;,&quot;settings&quot;:{&quot;cookie_name&quot;:&quot;&quot;,&quot;extra_selectors&quot;:&quot;&quot;}}],&quot;mobile_disabled&quot;:null,&quot;tablet_disabled&quot;:null,&quot;meta&quot;:{&quot;display&quot;:{&quot;stackable&quot;:false,&quot;overlay_disabled&quot;:false,&quot;scrollable_content&quot;:false,&quot;disable_reposition&quot;:false,&quot;size&quot;:&quot;normal&quot;,&quot;responsive_min_width&quot;:&quot;0%&quot;,&quot;responsive_min_width_unit&quot;:false,&quot;responsive_max_width&quot;:&quot;100%&quot;,&quot;responsive_max_width_unit&quot;:false,&quot;custom_width&quot;:&quot;640px&quot;,&quot;custom_width_unit&quot;:false,&quot;custom_height&quot;:&quot;380px&quot;,&quot;custom_height_unit&quot;:false,&quot;custom_height_auto&quot;:false,&quot;location&quot;:&quot;center&quot;,&quot;position_from_trigger&quot;:false,&quot;position_top&quot;:&quot;100&quot;,&quot;position_left&quot;:&quot;0&quot;,&quot;position_bottom&quot;:&quot;0&quot;,&quot;position_right&quot;:&quot;0&quot;,&quot;position_fixed&quot;:&quot;1&quot;,&quot;animation_type&quot;:&quot;fade&quot;,&quot;animation_speed&quot;:&quot;350&quot;,&quot;animation_origin&quot;:&quot;center top&quot;,&quot;overlay_zindex&quot;:false,&quot;zindex&quot;:&quot;1999999999&quot;},&quot;close&quot;:{&quot;text&quot;:&quot;&quot;,&quot;button_delay&quot;:&quot;0&quot;,&quot;overlay_click&quot;:false,&quot;esc_press&quot;:false,&quot;f4_press&quot;:false},&quot;click_open&quot;:[]}}" role="dialog" aria-hidden="true" aria-labelledby="pum_popup_title_63">

	<div id="popmake-63" class="pum-container popmake theme-57 pum-responsive pum-responsive-normal responsive size-normal pum-position-fixed">

				

				            <div id="pum_popup_title_63" class="pum-title popmake-title">
				Welcome to the DOGGIE BOWL™			</div>
		

		

				<div class="pum-content popmake-content" tabindex="0">
			<p style="text-align: center;"><strong>Before using the DOGGIE BOWL™ please ensure the following:<br>
</strong><span style="font-weight: 400;">1. Read our<a href="https://hosky.io/wp-content/uploads/2021/11/Brown-Paw-per-v0.69-Revision-420.pdf"><strong> Doggie Doo Doo</strong></a> (Brown Paw-per).<br>
</span><span style="font-weight: 400;">2. You are using a </span><span style="font-weight: 400;">Shell-Era wallet </span><span style="font-weight: 400;">that supports native assets.</span><span style="font-weight: 400;"><br>
</span><span style="font-weight: 400;">3. </span><span style="font-weight: 400;">Do </span><b>NOT</b><span style="font-weight: 400;">, we repeat </span><span style="font-weight: 400;">Do</span> <b>NOT</b><span style="font-weight: 400;"> send funds from an exchange, your funds could be lost, and you will not receive any $HOSKY.<br>
</span></p>
<pre><img loading="lazy" class="aligncenter wp-image-138 size-thumbnail" src="https://hosky.io/wp-content/uploads/2021/11/NEW-QR-150x150.png" alt="" width="150" height="150" srcset="https://hosky.io/wp-content/uploads/2021/11/NEW-QR-150x150.png 150w, https://hosky.io/wp-content/uploads/2021/11/NEW-QR-300x300.png 300w, https://hosky.io/wp-content/uploads/2021/11/NEW-QR-768x768.png 768w, https://hosky.io/wp-content/uploads/2021/11/NEW-QR.png 990w" sizes="(max-width: 150px) 100vw, 150px"></pre>
<p class="p1" style="text-align: center;"><strong>addr1vy740r73x2w3du2xxt76cs4hdml4zw2c5h7tddcyf3jauys9tyns4</strong></p>
<p><span style="font-weight: 400;">In order to receive $HOSKY Tokens please send EXACTLY 2 ADA to the provided address above, when you do, we will then return 1.5 ADA along with a random amount of $HOSKY between X &amp; X (See Chart At Bottom of Popup)</span></p>
<p><span style="font-weight: 400;">A portion of any dust remaining after the transaction fee will be donated to a doggo-related charity, we will allow the community to select the charity at a later time. Lastly, any amount above or below 2 ADA sent will be considered a doggy treat for the team, and for that we thank you.&nbsp;</span></p>
<p><span style="font-weight: 400;">– Woof!</span></p>
<p><em>* Halving has been implemented and the transaction queue keeps growing. Based on where in the queue your transaction is you could get some of the lower tiers.<br>
<img loading="lazy" class="aligncenter wp-image-224" src="https://hosky.io/wp-content/uploads/2021/11/2021-12-09_17-14-40.png" alt="" width="500" height="341" srcset="https://hosky.io/wp-content/uploads/2021/11/2021-12-09_17-14-40.png 742w, https://hosky.io/wp-content/uploads/2021/11/2021-12-09_17-14-40-300x205.png 300w" sizes="(max-width: 500px) 100vw, 500px"></em></p>
		</div>


				

				            <button type="button" class="pum-close popmake-close" aria-label="Close">
			×            </button>
		
	</div>

</div>
<div id="pum-161" class="pum pum-overlay pum-theme-61 pum-theme-content-only popmake-overlay click_open" data-popmake="{&quot;id&quot;:161,&quot;slug&quot;:&quot;cnft&quot;,&quot;theme_id&quot;:61,&quot;cookies&quot;:[],&quot;triggers&quot;:[{&quot;type&quot;:&quot;click_open&quot;,&quot;settings&quot;:{&quot;cookie_name&quot;:[&quot;pum-161&quot;],&quot;extra_selectors&quot;:&quot;&quot;}}],&quot;mobile_disabled&quot;:null,&quot;tablet_disabled&quot;:null,&quot;meta&quot;:{&quot;display&quot;:{&quot;stackable&quot;:false,&quot;overlay_disabled&quot;:false,&quot;scrollable_content&quot;:false,&quot;disable_reposition&quot;:false,&quot;size&quot;:&quot;medium&quot;,&quot;responsive_min_width&quot;:&quot;0%&quot;,&quot;responsive_min_width_unit&quot;:false,&quot;responsive_max_width&quot;:&quot;100%&quot;,&quot;responsive_max_width_unit&quot;:false,&quot;custom_width&quot;:&quot;640px&quot;,&quot;custom_width_unit&quot;:false,&quot;custom_height&quot;:&quot;380px&quot;,&quot;custom_height_unit&quot;:false,&quot;custom_height_auto&quot;:false,&quot;location&quot;:&quot;center top&quot;,&quot;position_from_trigger&quot;:false,&quot;position_top&quot;:&quot;100&quot;,&quot;position_left&quot;:&quot;0&quot;,&quot;position_bottom&quot;:&quot;0&quot;,&quot;position_right&quot;:&quot;0&quot;,&quot;position_fixed&quot;:false,&quot;animation_type&quot;:&quot;fade&quot;,&quot;animation_speed&quot;:&quot;350&quot;,&quot;animation_origin&quot;:&quot;center top&quot;,&quot;overlay_zindex&quot;:false,&quot;zindex&quot;:&quot;1999999999&quot;},&quot;close&quot;:{&quot;text&quot;:&quot;&quot;,&quot;button_delay&quot;:&quot;0&quot;,&quot;overlay_click&quot;:false,&quot;esc_press&quot;:false,&quot;f4_press&quot;:false},&quot;click_open&quot;:[]}}" role="dialog" aria-hidden="true">

	<div id="popmake-161" class="pum-container popmake theme-61 pum-responsive pum-responsive-medium responsive size-medium">

				

				

		

				<div class="pum-content popmake-content" tabindex="0">
			<p><img loading="lazy" class="alignnone size-full wp-image-162 aligncenter" src="https://hosky.io/wp-content/uploads/2021/11/CNFT.png" alt="" width="300" height="300" srcset="https://hosky.io/wp-content/uploads/2021/11/CNFT.png 300w, https://hosky.io/wp-content/uploads/2021/11/CNFT-150x150.png 150w" sizes="(max-width: 300px) 100vw, 300px"></p>
<p style="text-align: center;"><span style="color: #ffffff;">Guaranteed to be the biggest cash grab #CNFT has EVER seen.</span></p>
		</div>


				

				            <button type="button" class="pum-close popmake-close" aria-label="Close">
			×            </button>
		
	</div>

</div>
<script>document.body.classList.remove("no-js");</script>	<script>
	if ( -1 !== navigator.userAgent.indexOf( 'MSIE' ) || -1 !== navigator.appVersion.indexOf( 'Trident/' ) ) {
		document.body.classList.add( 'is-IE' );
	}
	</script>
	<script id="twenty-twenty-one-ie11-polyfills-js-after">
( Element.prototype.matches && Element.prototype.closest && window.NodeList && NodeList.prototype.forEach ) || document.write( '<script src="https://hosky.io/wp-content/themes/twentytwentyone/assets/js/polyfills.js?ver=1.4"></scr' + 'ipt>' );
</script>
<script src="https://hosky.io/wp-content/themes/twentytwentyone/assets/js/primary-navigation.js?ver=1.4" id="twenty-twenty-one-primary-navigation-script-js"></script>
<script src="https://hosky.io/wp-content/themes/twentytwentyone/assets/js/responsive-embeds.js?ver=1.4" id="twenty-twenty-one-responsive-embeds-script-js"></script>
<script src="https://hosky.io/wp-includes/js/jquery/ui/core.min.js?ver=1.12.1" id="jquery-ui-core-js"></script>
<script id="popup-maker-site-js-extra">
var pum_vars = {"version":"1.16.2","pm_dir_url":"https:\/\/hosky.io\/wp-content\/plugins\/popup-maker\/","ajaxurl":"https:\/\/hosky.io\/wp-admin\/admin-ajax.php","restapi":"https:\/\/hosky.io\/wp-json\/pum\/v1","rest_nonce":null,"default_theme":"54","debug_mode":"","disable_tracking":"","home_url":"\/","message_position":"top","core_sub_forms_enabled":"1","popups":[],"analytics_route":"analytics","analytics_api":"https:\/\/hosky.io\/wp-json\/pum\/v1"};
var pum_sub_vars = {"ajaxurl":"https:\/\/hosky.io\/wp-admin\/admin-ajax.php","message_position":"top"};
var pum_popups = {"pum-206":{"triggers":[{"type":"click_open","settings":{"cookie_name":"","extra_selectors":""}}],"cookies":[],"disable_on_mobile":false,"disable_on_tablet":false,"atc_promotion":null,"explain":null,"type_section":null,"theme_id":"54","size":"medium","responsive_min_width":"0%","responsive_max_width":"100%","custom_width":"640px","custom_height_auto":false,"custom_height":"380px","scrollable_content":false,"animation_type":"fade","animation_speed":"350","animation_origin":"center top","open_sound":"none","custom_sound":"","location":"center top","position_top":"100","position_bottom":"0","position_left":"0","position_right":"0","position_from_trigger":false,"position_fixed":false,"overlay_disabled":false,"stackable":false,"disable_reposition":false,"zindex":"1999999999","close_button_delay":"0","fi_promotion":null,"close_on_form_submission":false,"close_on_form_submission_delay":"0","close_on_overlay_click":false,"close_on_esc_press":false,"close_on_f4_press":false,"disable_form_reopen":false,"disable_accessibility":false,"theme_slug":"default-theme","id":206,"slug":"hosky-cash-grabnft"},"pum-63":{"triggers":[{"type":"click_open","settings":{"cookie_name":"","extra_selectors":""}}],"cookies":[],"disable_on_mobile":false,"disable_on_tablet":false,"atc_promotion":null,"explain":null,"type_section":null,"theme_id":"57","size":"normal","responsive_min_width":"0%","responsive_max_width":"100%","custom_width":"640px","custom_height_auto":false,"custom_height":"380px","scrollable_content":false,"animation_type":"fade","animation_speed":"350","animation_origin":"center top","open_sound":"none","custom_sound":"","location":"center","position_top":"100","position_bottom":"0","position_left":"0","position_right":"0","position_from_trigger":false,"position_fixed":true,"overlay_disabled":false,"stackable":false,"disable_reposition":false,"zindex":"1999999999","close_button_delay":"0","fi_promotion":null,"close_on_form_submission":false,"close_on_form_submission_delay":"0","close_on_overlay_click":false,"close_on_esc_press":false,"close_on_f4_press":false,"disable_form_reopen":false,"disable_accessibility":false,"theme_slug":"hello-box","id":63,"slug":"doggie-bowl"},"pum-161":{"triggers":[{"type":"click_open","settings":{"cookie_name":["pum-161"],"extra_selectors":""}}],"cookies":[],"disable_on_mobile":false,"disable_on_tablet":false,"atc_promotion":null,"explain":null,"type_section":null,"theme_id":"61","size":"medium","responsive_min_width":"0%","responsive_max_width":"100%","custom_width":"640px","custom_height_auto":false,"custom_height":"380px","scrollable_content":false,"animation_type":"fade","animation_speed":"350","animation_origin":"center top","open_sound":"none","custom_sound":"","location":"center top","position_top":"100","position_bottom":"0","position_left":"0","position_right":"0","position_from_trigger":false,"position_fixed":false,"overlay_disabled":false,"stackable":false,"disable_reposition":false,"zindex":"1999999999","close_button_delay":"0","fi_promotion":null,"close_on_form_submission":false,"close_on_form_submission_delay":"0","close_on_overlay_click":false,"close_on_esc_press":false,"close_on_f4_press":false,"disable_form_reopen":false,"disable_accessibility":false,"theme_slug":"content-only","id":161,"slug":"cnft"}};
</script>
<script src="//hosky.io/wp-content/uploads/pum/pum-site-scripts.js?defer&amp;generated=1639962930&amp;ver=1.16.2" id="popup-maker-site-js"></script>
<script src="https://hosky.io/wp-includes/js/wp-embed.min.js?ver=5.8.3" id="wp-embed-js"></script>
	<script>
	/(trident|msie)/i.test(navigator.userAgent)&&document.getElementById&&window.addEventListener&&window.addEventListener("hashchange",(function(){var t,e=location.hash.substring(1);/^[A-z0-9_-]+$/.test(e)&&(t=document.getElementById(e))&&(/^(?:a|select|input|button|textarea)$/i.test(t.tagName)||(t.tabIndex=-1),t.focus())}),!1);
	</script>
	


</body></html>
