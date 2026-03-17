---
layout: default
permalink: /
lang: en
published: true
---


# Select Language

- [English]({{ '/en/' | relative_url }})
- [Deutsch]({{ '/de/' | relative_url }})

If you are not redirected automatically, choose your language above.

<script>
	(function () {
		var selectedLang = 'en';

		try {
			var savedLang = localStorage.getItem('preferredLang');
			if (savedLang === 'en' || savedLang === 'de') {
				selectedLang = savedLang;
			} else {
				var browserLang = (navigator.languages && navigator.languages[0]) || navigator.language || 'en';
				if (browserLang.toLowerCase().indexOf('de') === 0) {
					selectedLang = 'de';
				}
				localStorage.setItem('preferredLang', selectedLang);
			}
		} catch (e) {
			var fallbackBrowserLang = (navigator.languages && navigator.languages[0]) || navigator.language || 'en';
			if (fallbackBrowserLang.toLowerCase().indexOf('de') === 0) {
				selectedLang = 'de';
			}
		}

		window.location.replace('{{ '/' | relative_url }}' + selectedLang + '/');
	})();
</script>

<noscript>
	<meta http-equiv="refresh" content="0; url={{ '/en/' | relative_url }}">
</noscript>
