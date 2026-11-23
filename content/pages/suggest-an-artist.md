---
title: "ఒక కళాకారుడిని సూచించండి"
slug: suggest-an-artist
---

యేసును అనుసరించే సంగీతకారుల గురించి, కళాకారుల గురించి వినడం నాకు చాలా ఇష్టం. నేను ఎవరి గురించి రాయాలని, ఎవరిని ఇంటర్వ్యూ చేయాలని, లేదా ఎవరి గురించి ప్రతిస్పందన వీడియో చేయాలని మీరు కోరుకుంటున్నారో, అలాంటి వారిని మీకు తెలిస్తే ఇక్కడ నాకు చెప్పండి.

ఒక పేరు, ఒక లింకు చాలు — ఎందుకు ఆ వ్యక్తి అని కొన్ని మాటల్లో చెప్పండి. వచ్చేవన్నీ నేను చదువుతాను. చాలా ధన్యవాదాలు.

మీకు తెలిసిన వారున్నారా? వారి ఫోటోను తాకండి, ఫారం తనంతట తాను నిండుతుంది — తర్వాత ఎందుకు ఆ వ్యక్తి అని కొన్ని మాటల్లో చేర్చి పంపండి.

<div class="suggest-carousel" role="list" aria-label="మీరు సూచించగల సంగీతకారులు, కళాకారులు">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }}ను సూచించండి">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">లేదా కింద కొత్త వారిని సూచించండి — నేను వినాలని మీరు అనుకునే ఎవరినైనా.</p>

ఈ సైట్ 18 ఏళ్లలోపు వారి కోసం కాదు.

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">కళాకారుడి పేరు</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="నేను ఎవరిని చూడాలి?" required>

  <label for="suggest-link">సోషల్ మీడియా ప్రొఫైల్ లింకు</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>వారితో నేను ఏమి చేయాలి?</legend>
    <label><input type="checkbox" name="kind" value="write"> వారి గురించి రాయండి</label>
    <label><input type="checkbox" name="kind" value="interview"> వారిని ఇంటర్వ్యూ చేయండి</label>
    <label><input type="checkbox" name="kind" value="reaction"> వారి గురించి ప్రతిస్పందన వీడియో చేయండి</label>
  </fieldset>

  <label for="suggest-why">ఎందుకు ఆ వ్యక్తి?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="కొన్ని మాటలు చాలు…"></textarea>

  <label for="suggest-name">మీ పేరు <span class="optional">(ఐచ్ఛికం)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="నేను ధన్యవాదాలు చెప్పడానికి">

  <label for="suggest-from-link">మీ సోషల్ మీడియా ప్రొఫైల్ లింకు <span class="optional">(ఐచ్ఛికం)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">సూచన పంపండి</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
