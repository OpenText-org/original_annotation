# OpenText.org Original Annotation



## Base level

* The base level XML contains:
	1. milestone elements for **chapter** and **verse** segments
	2. `<w>` word elements that contain:
		1. part-of-speech information `<pos>`
		2. word form information `<wf>` - **N.B.** for copyright reasons inflected forms are missing*
		3. semantic domain informaion `<sem>`

* Example segment of base XML:

```
<book name="Phlm">
  <chapter sID="NT.Phlm.1" num="1"/>
  <verse sID="NT.Phlm.1.1" num="1"/>
  <w xml:id="NT.Phlm.w1" ref="NT.Phlm.1.1">
    <pos>
      <NON num="sing" cas="nom" gen="mas"/>
    </pos>
    <wf betaLex="*pau=los" lex="Παῦλος"></wf>
    <sem>
      <domain majorNum="93" subNum="294"/>
    </sem>
  </w>
  <w xml:id="NT.Phlm.w2" ref="NT.Phlm.1.1">
    <pos>
      <NON num="sing" cas="nom" gen="mas"/>
    </pos>
    <wf betaLex="de/smios" lex="δέσμιος"></wf>
    <sem>
      <domain majorNum="37" subNum="117"/>
    </sem>
  </w>
  <w xml:id="NT.Phlm.w3" ref="NT.Phlm.1.1">
    <pos>
      <NON num="sing" cas="gen" gen="mas"/>
    </pos>
    <wf betaLex="*xristo/s" lex="Χριστός"></wf>
    <sem>
      <domain majorNum="93" subNum="387"/>
      <domain majorNum="53" subNum="82"/>
    </sem>
  </w>

  ....
```


### Word group annotation


* Example segment of word group XML:


```
<chapter xmlns:xlink="http://www.w3.org/1999/xlink" book="Phlm" num="1">
  <wg.groups>
    <wg.group xml:id="NT.Phlm.1_wg1">
      <wg.head>
        <wg.word xlink:href="NT.Phlm.w1">
          <wg.modifiers>
            <wg.definer>
              <wg.word xlink:href="NT.Phlm.w2">
                <wg.modifiers>
                  <wg.qualifier>
                    <wg.word xlink:href="NT.Phlm.w3">
                      <wg.modifiers>
                        <wg.definer>
                          <wg.word xlink:href="NT.Phlm.w4"/>
                        </wg.definer>
                      </wg.modifiers>
                    </wg.word>
                  </wg.qualifier>
                </wg.modifiers>
              </wg.word>
            </wg.definer>
          </wg.modifiers>
        </wg.word>
      </wg.head>
    </wg.group>
```

* This is the first word group in Philemon and is represented in the word group box diagrams like this:

![](wg_example.png)

### Clause level
