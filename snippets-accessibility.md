# CSS für den Workshop zur Barrierefreiheit

## Screenreader only Klassen

```css
/*
	Improved screen reader only CSS class
	@author Gaël Poupard
		@note Based on Yahoo!'s technique
		@author Thierry Koblentz
		@see https://developer.yahoo.com/blogs/ydn/clip-hidden-content-better-accessibility-53456.html
	* 1.
		@note `clip` is deprecated but works everywhere
		@see https://developer.mozilla.org/en-US/docs/Web/CSS/clip
	* 2.
		@note `clip-path` is the future-proof version, but not very well supported yet
		@see https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path
		@see http://caniuse.com/#search=clip-path
		@author Yvain Liechti
		@see https://twitter.com/ryuran78/status/778943389819604992
	* 3.
		@note preventing text to be condensed
		author J. Renée Beach
		@see https://medium.com/@jessebeach/beware-smushed-off-screen-accessible-text-5952a4c2cbfe
		@note Drupal 8 goes with word-wrap: normal instead
		@see https://www.drupal.org/node/2045151
		@see http://cgit.drupalcode.org/drupal/commit/?id=5b847ea
	* 4.
		@note !important is important
		@note Obviously you wanna hide something
		@author Harry Roberts
		@see https://csswizardry.com/2016/05/the-importance-of-important/
*/

.sr-only {
  border: 0 !important;
  clip: rect(1px, 1px, 1px, 1px) !important; /* 1 */
  -webkit-clip-path: inset(50%) !important;
  clip-path: inset(50%) !important; /* 2 */
  height: 1px !important;
  margin: -1px !important;
  overflow: hidden !important;
  padding: 0 !important;
  position: absolute !important;
  width: 1px !important;
  white-space: nowrap !important; /* 3 */
}

/*
	Use in conjunction with .sr-only to only display content when it's focused.
	@note Useful for skip links 
	@see http://www.w3.org/TR/2013/NOTE-WCAG20-TECHS-20130905/G1
	@note Based on a HTML5 Boilerplate technique, included in Bootstrap
	@note Fixed a bug with position: static on iOS 10.0.2 + VoiceOver
		@author Sylvain Pigeard
		@see https://github.com/twbs/bootstrap/issues/20732
*/
.sr-only-focusable:focus,
.sr-only-focusable:active {
  clip: auto !important;
  -webkit-clip-path: none !important;
  clip-path: none !important;
  height: auto !important;
  margin: auto !important;
  overflow: visible !important;
  width: auto !important;
  white-space: normal !important;
}
.invisible {
  display: none !important;
}
```

## Simulation von Fehlsichtigkeiten

```css
/*
	Diseases Simulation by CSS-Class
	@author Michael Reichart
	@note A Physiologically-based Model for Simulation of Color Vision Deficiency
	@author Gustavo M. Machado
  @author Manuel M. Oliveira
  @author Leandro A. F. Fernandes
  @see https://www.inf.ufrgs.br/~oliveira/pubs_files/CVD_Simulation/CVD_Simulation.html 
*/
.blurred-vision {
  filter: blur(2px);
}
.achromatopsia {
  filter: url('data:image/svg+xml,\
      <svg xmlns="http://www.w3.org/2000/svg">\
        <filter id="achromatopsia">\
          <feColorMatrix values="0.213  0.715  0.072  0.000  0.000\
                                 0.213  0.715  0.072  0.000  0.000\
                                 0.213  0.715  0.072  0.000  0.000\
                                 0.000  0.000  0.000  1.000  0.000" />\
        </filter>\
      </svg>#achromatopsia');
}

.deuteranopia {
  filter: url('data:image/svg+xml,\
      <svg xmlns="http://www.w3.org/2000/svg">\
        <filter id="deuteranopia">\
          <feColorMatrix values="0.367  0.861 -0.228  0.000  0.000\
                                 0.280  0.673  0.047  0.000  0.000\
                                -0.012  0.043  0.969  0.000  0.000\
                                 0.000  0.000  0.000  1.000  0.000" />\
        </filter>\
      </svg>#deuteranopia');
}

.protanopia {
  filter: url('data:image/svg+xml,\
      <svg xmlns="http://www.w3.org/2000/svg">\
        <filter id="protanopia">\
        <feColorMatrix values="0.152  1.053 -0.205  0.000  0.000\
                               0.115  0.786  0.099  0.000  0.000\
                              -0.004 -0.048  1.052  0.000  0.000\
                               0.000  0.000  0.000  1.000  0.000" />\
        </filter>\
      </svg>#protanopia');
}

.tritanopia {
  filter: url('data:image/svg+xml,\
      <svg xmlns="http://www.w3.org/2000/svg">\
        <filter id="tritanopia">\
        <feColorMatrix values="1.256 -0.077 -0.179  0.000  0.000\
                              -0.078  0.931  0.148  0.000  0.000\
                               0.005  0.691  0.304  0.000  0.000\
                               0.000  0.000  0.000  1.000  0.000" />\
        </filter>\
      </svg>#tritanopia');
}
```
