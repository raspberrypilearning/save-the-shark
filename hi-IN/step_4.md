## शार्क के स्वास्थ्य की निगरानी करें

इस चरण में, आप स्वास्थ्य बिंदु शामिल करने के लिए `variable`{:class="block3variables"} का उपयोग करेंगे। अगर शार्क गलती से प्लास्टिक कचरा खा लेगी तो उसका स्वास्थ्य गिर जाएगा।

--- task ---

एक नया new `variable`{:class="block3variables" बनाएं, जिसे `health` कहा जाता है।

--- /task ---

--- task ---

Sprite सूची में **Shark** स्प्राइट पर क्लिक करें। ब्लॉक जोड़ें ताकि जब खेल शुरू हो, तो शार्क का स्वास्थ्य `20` पर सेट हो, और जब शार्क का स्वास्थ्य `0` से नीचे चला जाए, तो खेल समाप्त हो जाए:

![shark स्प्राइट](images/shark-sprite.png)

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

**Plastic** स्प्राइट पर वापस जाएं। यदि वह गलती से कोई प्लास्टिक खा लेता है को शार्क के स्वस्थ को `-5` तक कम करने के लिए कुछ कोड जोड़ें:

![plastic स्प्राइट](images/plastic-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (Shark v)> then
change (health v) by (-5)
delete this clone
```

--- /task ---

--- task ---

यह जांचने के लिए प्रोग्राम को फिर से चलाएँ कि अगर शार्क प्लास्टिक खाती है तो उसका स्वास्थ्य कम हो जाता है।

--- /task ---

--- save ---
