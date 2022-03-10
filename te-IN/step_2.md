## సొరచేపని కదిలించండి

ఈ దశలో, Stage పై సొరచేప కదలికను నియంత్రించడానికి మౌస్‌ని ఉపయోగించేందుకు ప్లేయర్‌ని అనుమతించడానికి మీరు కోడ్‌ని జోడిస్తారు.

--- task ---

**Online:** Scratch లో [స్టార్టర్ ప్రాజెక్ట్ ](http://rpf.io/save-the-shark-on){:target="_blank"} ని తెరవండి.

**Offline:** Scratch యొక్క ఆఫ్ లైన్ ఎడిటర్ లో [ప్రాజెక్టు స్టార్టర్ ఫైల్](http://rpf.io/p/te-IN/save-the-shark-get){:target="_blank"} ని తెరవండి. మీకు అవసరమైతే, మీరు [ఇక్కడ Scratch ను డౌన్ లోడ్ చేసి ఇన్‌స్టాల్ చేయవచ్చు.](https://scratch.mit.edu/download){:target="_blank"}.

--- /task ---

స్టార్టర్ ప్రాజెక్ట్‌లో, మీరు జలాంతర నేపథ్యంలో **Shark** sprite ను చూడవచ్చు.

![స్టార్టర్ ప్రాజెక్ట్](images/starter_project.png)

--- task ---

ఆకుపచ్చ జెండాను క్లిక్ చేసినప్పుడు, సొరచేప Stage దిగువన ప్రారంభించాలి. ఈ కోడ్‌ని జోడించండి, తద్వారా **Shark** sprite సరైన స్థానంలో ప్రారంభమవుతుంది:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
```

--- /task ---

ఈ ప్రాజెక్ట్‌ను మొబైల్ పరికరాలకు అనుకూలంగా చేయడానికి, మీరు ఎడమ మౌస్ బటన్‌ను నొక్కినప్పుడు లేదా వేలు స్క్రీన్‌ను తాకినప్పుడు, సొరచేప కదలికను నియంత్రించడానికి కర్సర్ స్థానాన్ని ఉపయోగిస్తారు. అదృష్టవశాత్తూ, Scratch యొక్క `mouse down`{:class="block3sensing"} బ్లాక్ మౌస్ బటన్‌లపై మరియు టచ్‌స్క్రీన్‌లపై వేళ్లకు పని చేస్తుంది!

--- task ---

ఎడమ మౌస్ బటన్‌ను నొక్కినప్పుడు మీ ప్రోగ్రామ్ నిరంతరం గుర్తించవలసి ఉంటుంది. దీనికోసం, `forever`{:class="block3control"} లూప్‌ని స్క్రిప్ట్ కి జోడించి, ఆపై `if ... then`{:class="block3control"} బ్లాక్‌ని, `mouse down`{:class="block3sensing"} ని గుర్తించడానికి ఉపయోగించండి:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+forever
if <mouse down?> then
```

--- /task ---

--- task ---

**Shark** sprite స్థానం కంటే Stage కి ఎడమ వైపుకు దగ్గరగా క్లిక్ చేస్తే, **Shark** sprite ఎడమవైపుకు కదులుతుంది.

X అక్షం వెంట కర్సర్ యొక్క స్థానం `mouse x`{:class="block3sensing"} బ్లాక్‌లో నిల్వ చేయబడినందున ఈ చర్య సాధ్యమవుతుంది.

యూజర్ ఎక్కడ క్లిక్ చేస్తారో దానికి ప్రోగ్రామ్‌ ప్రతిస్పందించేలా చేయడానికి, క్రింది బ్లాక్‌లను జోడించండి: `if`{:class="block3control"} `mouse x`{:class="block3sensing"} **Shark** sprite యొక్క `x position `{:class="block3motion"} కంటే `less than `{:class=" block3operators"} ఉంటే `then`{:class="block3control"} sprite ఎడమవైపుకు వెళ్లడానికి `change x by`{:class="block3motion"} `-10` కి మార్చాలి:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
+if <(mouse x) < (x position)> then
change x by (-10)
next costume
```

--- /task ---

--- task ---

మీరు షార్క్ ఎడమవైపు క్లిక్ చేసినప్పుడు షార్క్ ఎడమవైపుకు కదులుతుందో లేదో పరీక్షించడానికి ప్రోగ్రామ్‌ను అమలు చేయడానికి ఆకుపచ్చ జెండాపై క్లిక్ చేయండి.

--- /task ---

--- task ---

మౌస్ క్లిక్ చేసినప్పుడు `if`{:class="block3control"} `mouse x`{:class="block3sensing"} `x position`{:class="block3motion"} కంటే `greater than `{:class="block3operators"} ఉంటే `then`{:class="block3control"} sprite **Shark** కుడి వైపుకు వెళ్లడానికి `change x by`{:class="block3motion"} `10` కి మార్చాలి. కింది బ్లాక్‌లను జోడించండి:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
change x by (-10)
next costume
end
+if <(mouse x) > (x position)> then
change x by (10)
next costume
```

--- /task ---

--- task ---

మీరు షార్క్ కుడివైపు క్లిక్ చేసినప్పుడు షార్క్ కుడివైపుకి కదులుతుందో లేదో పరీక్షించడానికి ప్రోగ్రామ్‌ను అమలు చేయడానికి ఆకుపచ్చ జెండాపై క్లిక్ చేయండి.

--- /task ---

--- save ---
