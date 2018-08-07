---
title: "Kontakt mig"
weight: 9
menuname: "Kontakt mig"
draft: false
---

<form id="contactform" method="post" action="https://formspree.io/juri@juri.dk">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="Navn"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="4" placeholder="Meddelelse"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Send besked" class="special" /></li>
		<li><input type="reset" value="Nulstil" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Kontakt via juri.dk" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">Tak for din henvendelse!</span>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>


{{< socialLinks >}}
