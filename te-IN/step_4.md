## సొరచేప ఆరోగ్యాన్ని పర్యవేక్షించండి

ఈ దశలో, మీరు హెల్త్ పాయింట్‌లను చేర్చడానికి `variable`{:class="block3variables"}ని ఉపయోగిస్తారు. పొరపాటున ప్లాస్టిక్ వ్యర్థాలను తింటే షార్క్ ఆరోగ్యం తగ్గిపోతుంది.

--- task ---

`health` అనే కొత్త `variable`{:class="block3variables"} (వేరియబుల్) ని సృష్టించండి.

--- /task ---

--- task ---

Sprite జాబితాలో **Shark** sprite పై క్లిక్ చేయండి. బ్లాక్‌లను జోడించండి, తద్వారా గేమ్ ప్రారంభమైనప్పుడు, షార్క్ ఆరోగ్యం `20` కి సెట్ చేయబడుతుంది మరియు షార్క్ ఆరోగ్యం `0` కంటే తక్కువగా ఉన్నప్పుడు, గేమ్ ముగుస్తుంది:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+set (health v) to (20)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
change x by (-10)
end
if <(mouse x) > (x position)> then
change x by (10)
end
+if <(health) < (0)> then
stop (all v)
```

--- /task ---

--- task ---

**Plastic** sprite కి తిరిగి వెళ్లండి. షార్క్ పొరపాటున ఏదైనా ప్లాస్టిక్‌ని తింటే దాని ఆరోగ్యాన్ని `-5` పాయింట్లు తగ్గించడానికి కొంత కోడ్‌ ను జోడించండి:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (Shark v)> then
change (health v) by (-5)
delete this clone
```

--- /task ---

--- task ---

షార్క్ ప్లాస్టిక్ తింటే దాని ఆరోగ్యం తగ్గిపోతుందని పరీక్షించడానికి ప్రోగ్రామ్‌ను మళ్లీ అమలు చేయండి.

--- /task ---

--- save ---
