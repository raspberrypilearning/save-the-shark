## प्लास्टिक कचरा जोडा

या टप्प्यात, तुम्ही तुमच्या गेममध्ये प्लास्टिकचा कचरा जोडाल.

Stage खालील Sprite लीस्टमध्ये, प्लास्टीक बॉटल सारख्या दिसणाऱ्या स्प्राईटवर क्लिक करा. या स्प्राईटला चार कॉश्चुम आहेत: बॉटल, रॅपर, बॅग आणि प्लास्टीक कॅन होल्डर.

--- task ---

हिरव्या झेंड्यावर क्लिक केल्यावर, **Plastic** स्प्राईटने Stage च्या वर हलायला हवे आणि त्यानंतर `hide`{:class="block3looks"}. **Plastic** स्प्राईटला खालील कोड जोडा:

![plastic स्प्राईट](images/plastic-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (200)
hide
```

--- /task ---

--- task ---

**Plastic** स्प्राईटला आता स्वतःचे कोणतेही क्लोन्स तयार करण्याची आवश्यकता आहे. खालील कोड जोडा:

![plastic स्प्राईट](images/plastic-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (200)
hide
+forever
create clone of (myself v)
wait (pick random (1) to (5)) seconds
```

--- /task ---

--- task ---

क्लोन तयार झाल्यावर, क्लोनने स्वतःचा `show`{:class="block3looks"} दाखवावे, `random`{:class="block3operators"} `costume`{:class="block3looks"} निवडा, त्यानंतर `random`{:class="block3operators"} `x`{:class="block3motion"} पोजिशनला जा. नवीन स्क्रिप्ट म्हणून खालील कोड जोडा:

![plastic स्प्राईट](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (200)
```

--- /task ---

--- task ---

तुम्हाला Stage च्या खालील भागाकडे `random`{:class="block3operators"} वेगाने जाणारे प्लास्टीक हवे आहे, त्यामुळे नवीन `variable`{:class="block3variables"} तयार करा ज्याला `speed` म्हणतात. ते `For this sprite only` सेट करा:

![नवीन व्हेरिएबल मेनू](images/speed-variable.png)



--- /task ---

--- task ---

`speed`{:class="block3variables"} `random`{:class="block3operators"} संख्या असण्यासाठी सेट करा. `repeat until`{:class="block3control"} ब्लॉक वापरा जो क्लोन y अक्षावर (stage च्या खाली) `-180` वर केव्हा पोहोचतो ते ठरवेल. क्लोन Stage च्या खाली `speed`{:class="block3variables"} व्हेरिएबल वापरून हलवा. आणि शेवटी, `wait`{:class="block3control"} ब्लॉक जोडा `0.1` सेकंद व्हॅल्यूसह जेणेकरून तुम्ही हालचाल बघू शकता:

![plastic स्प्राईट](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (200)
+set (speed v) to (pick random (-1) to (-10))
+repeat until <(y position) < (-180)>
change y by (speed)
wait (0.1) seconds

```

--- /task ---

तुमचा गेम रन करा, आणि तुम्ही Stage च्या वरच्या भागातून कोणत्याही वेगाने आणि कोणत्याही पोजिशन मधून पडणारा प्लास्टीक कचरा बघायला हवा. कचरा Stage च्या खालच्या भागात जमा होतो, आणि तेथेच रहातो ही समस्या आहे.

--- task ---

`delete this clone`{:class="block3control"} ब्लॉक जोडा जेणेकरून **Plastic** स्प्राईट्स Stage च्या खाली हिट होतो त्यावेळी स्वतःच डिलीट होईल:

![plastic स्प्राईट](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (200)
set (speed v) to (pick random (-1) to (-10))
repeat until <(y position) < (-180)>
change y by (speed)
wait (0.1) seconds
end
+delete this clone
```

--- /task ---

--- save ---

