###Reproduction sample for Chromium issue 543957###

git clone https://github.com/davemckeown/chromium-543957-repro
cd chromium-543957-repro
python -m SimpleHTTPServer 8080

Open localhost:8080 in Chrome

**Issue details:**
https://code.google.com/p/chromium/issues/detail?id=543957

**Expected behaviour:**

- Searching for "searchMethodName" on the sources tab in chrome developers tools should include all instances of the string "searchMethodName" in the current web page
- This example should include four search results for the string "searchMethodName"

**Expected search results:**

- main.js line 1
- main.js line 2
- index.html line 20
- index.html line 21

**Observed behaviour:**

- Search results are incomplete and do not include searchMethodName_543957_example from line 20 in index.html
- Only instances of strings with "searchMethodName" from externally included source files show up in developer tools search

**Observed search results:**

- main.js line 1
- main.js line 2