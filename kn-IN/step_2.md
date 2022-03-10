## ಶಾರ್ಕ್‌ನ್ನು ಚಲಿಸಿ

ಈ ಹಂತದಲ್ಲಿ, ಆಟಗಾರ Stage ಮೇಲೆ ಶಾರ್ಕ್‌ನ ಚಲನೆಯನ್ನು ನಿಯಂತ್ರಿಸಲು ಮೌಸ್‌ ಉಪಯೋಗಿಸಲು ಅನುವುಮಾಡಿಕೊಡಲು ನೀವು ಕೋಡ್‌ ಸೇರಿಸುತ್ತೀರಿ.

--- task ---

**ಆನ್‌ಲೈನ್:** Scratch ನಲ್ಲಿ [ಪ್ರಾರಂಭಿಕ ಪ್ರಾಜೆಕ್ಟ್](http://rpf.io/save-the-shark-on){:target="_blank"} ತೆರೆಯಿರಿ.

**ಆಫ್‌ಲೈನ್:** Scratch ಆಫ್‌ಲೈನ್‌ ಎಡಿಟರ್‌ನಲ್ಲಿ [ಪ್ರಾರಂಭಿಕ ಪ್ರಾಜೆಕ್ಟ್‌ ಫೈಲ್](http://rpf.io/p/en/save-the-shark-get){:target="_blank"} ತೆರೆಯಿರಿ. ನಿಮಗೆ ಬೇಕಾದರೆ, ನೀವು [ಇಲ್ಲಿ Scratch ಡೌನ್‌ಲೋಡ್‌ ಮಾಡಿಕೊಂಡು ಇನ್‌ಸ್ಟಾಲ್‌ ಮಾಡಬಹುದು](https://scratch.mit.edu/download){:target="_blank"}.

--- /task ---

ಪ್ರಾರಂಭಿಕ ಪ್ರಾಜೆಕ್ಟ್‌ನಲ್ಲಿ, ನೀವು ನೀರಿನೊಳಗಿನ ಹಿನ್ನೆಲೆಯಲ್ಲಿ **Shark** ಸ್ಪ್ರೈಟ್‌ ನೋಡಬೇಕು.

![ಪ್ರಾರಂಭಿಕ ಪ್ರಾಜೆಕ್ಟ್](images/starter_project.png)

--- task ---

ಹಸಿರು ಬಾವುಟವನ್ನು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ, ಶಾರ್ಕ್‌ ಸ್ಟೇಜ್‌ನ ಕೆಳಗಡೆಯಿಂದ ಪ್ರಾರಂಭಿಸಬೇಕು. **Shark** ಸ್ಪ್ರೈಟ್‌ ಸರಿಯಾದ ಸ್ಥಾನದಲ್ಲಿ ಪ್ರಾರಂಭಿಸಲು ಈ ಕೋಡ್‌ನ್ನು ಸೇರಿಸಿ:

![ಶಾರ್ಕ್‌ ಸ್ಪ್ರೈಟ್](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
```

--- /task ---

ಈ ಪ್ರಾಜೆಕ್ಟ್‌ ಮೊಬೈಲ್‌ ಸಾಧನಗಳಿಗೆ ಸೂಕ್ತವಾಗುವಂತೆ ಮಾಡಲು, ಶಾರ್ಕ್‌ನ ಚಲನೆಯನ್ನು ನಿಯಂತ್ರಿಸಲು, ಮೌಸ್‌ನ ಎಡ ಬಟನ್‌ ಒತ್ತಿದಾಗ ಅಥವಾ ಬೆರಳು ಪರದೆಯನ್ನು ಸ್ಪರ್ಶಿಸಿದಾಗ ನೀವು ಕರ್ಸರ್‌ನ ಸ್ಥಳವನ್ನು ಉಪಯೋಗಿಸುತ್ತೀರಿ. ಅದೃಷ್ಟವಶಾತ್, Scratch ನ `mouse down`{:class="block3sensing"} ಬ್ಲಾಕ್‌ ಮೌಸ್‌ ಬಟನ್‌ಗಳ ಮೇಲೆ ಮತ್ತು ಟಚ್‌ಸ್ಕ್ರೀನ್‌ಗಳ ಮೇಲೆ ಬೆರಳುಗಳು ಎರಡಕ್ಕೂ ಕೆಲಸಮಾಡುತ್ತದೆ!

--- task ---

ಮೌಸ್‌ನ ಎಡ ಬಟನ್‌ ಒತ್ತಿದಾಗ ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಮ್‌ ನಿರಂತರವಾಗಿ ಪತ್ತೆಹಚ್ಚಬೇಕು. ಇದನ್ನು ಮಾಡಲು, ನಿಮ್ಮ ಬರಹಕ್ಕೆ `forever`{:class="block3control"} ಲೂಪ್‌ನ್ನು ಸೇರಿಸಿ, ನಂತರ `if ... then`{:class="block3control"} ಬ್ಲಾಕ್‌ನ್ನು `mouse down`{:class="block3sensing"} ಆಗಿದೆಯೇ ಎಂದು ಪತ್ತೆಹಚ್ಚಲು ಉಪಯೋಗಿಸಿ:

![ಶಾರ್ಕ್‌ ಸ್ಪ್ರೈಟ್](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+forever
if <mouse down?> then
```

--- /task ---

--- task ---

ಬಳಕೆದಾರ ಕರ್ಸರ್‌ನ್ನು **Shark** ಸ್ಪ್ರೈಟ್‌ನ ಸ್ಥಾನಕ್ಕಿಂತ Stage ನ ಎಡ ಭಾಗದಲ್ಲಿ ಕ್ಲಿಕ್‌ ಮಾಡಿದರೆ, ಆಗ **Shark** ಸ್ಪ್ರೈಟ್‌ ಎಡಕ್ಕೆ ಚಲಿಸುತ್ತದೆ.

ಈ ಕ್ರಿಯೆ ಸಾಧ್ಯವಾಗುತ್ತದೆ ಏಕೆಂದರೆ x ಅಕ್ಷದ ಉದ್ದಕ್ಕೂ ಕರ್ಸರ್‌ನ ಸ್ಥಾನ `mouse x`{:class="block3sensing"} ಬ್ಲಾಕ್‌ನಲ್ಲಿ ಸಂಗ್ರಹವಾಗಿದೆ.

ಬಳಕೆದಾರ ಎಲ್ಲಿ ಕ್ಲಿಕ್‌ ಮಾಡುತ್ತಾನೆ ಗೆ ಪ್ರೋಗ್ರಾಮ್‌ ಪ್ರತಿಕ್ರಿಯಿಸುವಂತೆ ಮಾಡಲು, ಈ ಕೆಳಗಿನ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ: `if`{:class="block3control"} `mouse x`{:class="block3sensing"} `less than`{:class="block3operators"} **Shark** ಸ್ಪ್ರೈಟ್‌ನ `x position`{:class="block3motion"} ಆದರೆ, `then`{:class="block3control"} ಆಗ ಸ್ಪ್ರೈಟ್‌ ಎಡಕ್ಕೆ ಚಲಿಸಲು `change x by`{:class="block3motion"} `-10` ಬದಲಾಯಿಸಬೇಕು:

![ಶಾರ್ಕ್‌ ಸ್ಪ್ರೈಟ್](images/shark-sprite.png)

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

ಶಾರ್ಕ್‌ನ ಎಡಕ್ಕೆ ನೀವು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಶಾರ್ಕ್‌ ಎಡಕ್ಕೆ ಚಲಿಸುತ್ತದೆಯೇ ಎಂದು ಪರೀಕ್ಷಿಸಲು ಪ್ರೋಗ್ರಾಮ್‌ ರನ್‌ ಮಾಡಲು ಹಸಿರು ಬಾವುಟದ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ.

--- /task ---

--- task ---

ಮೌಸ್‌ನ್ನು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ, `if`{:class="block3control"} `mouse x`{:class="block3sensing"} `greater than`{:class="block3operators"} `x position`{:class="block3motion"} ಆದರೆ, `then`{:class="block3control"} **Shark** ಸ್ಪ್ರೈಟ್‌ ಬಲಕ್ಕೆ ಚಲಿಸಬೇಕು `change x by`{:class="block3motion"} `10`. ಈ ಕೆಳಗಿನ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ:

![ಶಾರ್ಕ್‌ ಸ್ಪ್ರೈಟ್](images/shark-sprite.png)

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

ಶಾರ್ಕ್‌ನ ಬಲಕ್ಕೆ ನೀವು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಶಾರ್ಕ್‌ ಬಲಕ್ಕೆ ಚಲಿಸುತ್ತದೆಯೇ ಎಂದು ಪರೀಕ್ಷಿಸಲು ಪ್ರೋಗ್ರಾಮ್‌ ರನ್‌ ಮಾಡಲು ಹಸಿರು ಬಾವುಟದ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ.

--- /task ---

--- save ---
