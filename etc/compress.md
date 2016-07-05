# Compress Comparsion


[lzop vs compress vs gzip vs bzip2 vs lzma vs lzma2/xz benchmark, reloaded][1]


[1]: http://stephane.lesimple.fr/blog/2010-07-20/lzop-vs-compress-vs-gzip-vs-bzip2-vs-lzma-vs-lzma2xz-benchmark-reloaded.html

#### Benchmark protocol

<table id="tablepress-1" class="tablepress tablepress-id-1"><thead><tr class="row-1 odd"><th class="column-1">program</th><th class="column-2">extension</th><th class="column-3">version</th><th class="column-4">comment</th><th class="column-5">supported compression levels</th></tr></thead><tbody class="row-hover"><tr class="row-2 even"><td class="column-1"><a href="http://www.lzop.org/">lzop</a></td><td class="column-2">.lzop</td><td class="column-3">1.02rc1</td><td class="column-4">known to be very fast</td><td class="column-5">1 to 9, but 2 to 6 are equivalent, 3 by default</td></tr><tr class="row-3 odd"><td class="column-1"><a href="http://en.wikipedia.org/wiki/Compress">compress</a></td><td class="column-2">.Z</td><td class="column-3">4.2.4</td><td class="column-4">the legacy UNIX compression algorithm</td><td class="column-5">not configurable</td></tr><tr class="row-4 even"><td class="column-1"><a href="http://en.wikipedia.org/wiki/Gzip">gzip</a></td><td class="column-2">.gz (.tgz)</td><td class="column-3">1.3.12</td><td class="column-4">replaced compress in recent UNIX-like operating systems</td><td class="column-5">1 to 9, 6 by default</td></tr><tr class="row-5 odd"><td class="column-1"><a href="http://en.wikipedia.org/wiki/Bzip2">bzip2</a></td><td class="column-2">.bzip2 (.tbz, .tbz2)</td><td class="column-3">1.0.5</td><td class="column-4">known to have a better compression ratio than gzip, but much slower</td><td class="column-5">1 to 9, 9 by default</td></tr><tr class="row-6 even"><td class="column-1"><a href="http://en.wikipedia.org/wiki/Lzma">lzma</a></td><td class="column-2">.lzma</td><td class="column-3">4.999.9beta</td><td class="column-4">new algorithm aiming at high compression ratios</td><td class="column-5">0 to 9, 6 by default</td></tr><tr class="row-7 odd"><td class="column-1"><a href="http://en.wikipedia.org/wiki/Xz">lzma2</a></td><td class="column-2">.xz (.txz)</td><td class="column-3">4.999.9beta</td><td class="column-4">xz is a compression format, and uses by default the lzma2 algorithm, it has some  new features over lzma, for example integrity checking, as seen on the <a href="http://fr.wikipedia.org/wiki/Xz">French Wikipedia page</a></td><td class="column-5">0 to 9, 6 by default</td></tr></tbody></table>

#### Benchmark results

<div id="tablepress-2_wrapper" class="dataTables_wrapper no-footer"><table id="tablepress-2" class="tablepress tablepress-id-2 dataTable no-footer" role="grid" aria-describedby="tablepress-2_info"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody class="row-hover"><tr class="row-2 even" role="row"><td class="column-1">compress</td><td class="column-2">39.56</td><td class="column-3">2.64</td><td class="column-4">1 124</td><td class="column-5">1.60</td><td class="column-6">548</td></tr><tr class="row-3 odd" role="row"><td class="column-1">lzop-1</td><td class="column-2">36.17</td><td class="column-3">1.04</td><td class="column-4">1 004</td><td class="column-5">0.63</td><td class="column-6">?</td></tr><tr class="row-4 even" role="row"><td class="column-1">lzop-3</td><td class="column-2">36.38</td><td class="column-3">1.11</td><td class="column-4">940</td><td class="column-5">0.65</td><td class="column-6">?</td></tr><tr class="row-5 odd" role="row"><td class="column-1">lzop-7</td><td class="column-2">27.07</td><td class="column-3">13.15</td><td class="column-4">1 312</td><td class="column-5">0.70</td><td class="column-6">?</td></tr><tr class="row-6 even" role="row"><td class="column-1">lzop-8</td><td class="column-2">26.74</td><td class="column-3">27.67</td><td class="column-4">1 308</td><td class="column-5">0.65</td><td class="column-6">?</td></tr><tr class="row-7 odd" role="row"><td class="column-1">lzop-9</td><td class="column-2">26.73</td><td class="column-3">33.3</td><td class="column-4">1 308</td><td class="column-5">0.60</td><td class="column-6">?</td></tr><tr class="row-8 even" role="row"><td class="column-1">gzip-1</td><td class="column-2">28.72</td><td class="column-3">2.74</td><td class="column-4">708</td><td class="column-5">1.42</td><td class="column-6">486</td></tr><tr class="row-9 odd" role="row"><td class="column-1">gzip-2</td><td class="column-2">27.44</td><td class="column-3">2.90</td><td class="column-4">708</td><td class="column-5">1.42</td><td class="column-6">486</td></tr><tr class="row-10 even" role="row"><td class="column-1">gzip-3</td><td class="column-2">26.50</td><td class="column-3">3.22</td><td class="column-4">708</td><td class="column-5">1.40</td><td class="column-6">484</td></tr><tr class="row-11 odd" role="row"><td class="column-1">gzip-4</td><td class="column-2">24.77</td><td class="column-3">3.56</td><td class="column-4">708</td><td class="column-5">1.33</td><td class="column-6">486</td></tr></tbody></table></div></div>

<table id="tablepress-2" class="tablepress tablepress-id-2 dataTable no-footer" role="grid" aria-describedby="tablepress-2_info"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody class="row-hover"><tr class="row-12 even" role="row"><td class="column-1">gzip-5</td><td class="column-2">23.82</td><td class="column-3">4.43</td><td class="column-4">718</td><td class="column-5">1.27</td><td class="column-6">500</td></tr><tr class="row-13 odd" role="row"><td class="column-1">gzip-6</td><td class="column-2">23.43</td><td class="column-3">5.78</td><td class="column-4">716</td><td class="column-5">1.29</td><td class="column-6">488</td></tr><tr class="row-14 even" role="row"><td class="column-1">gzip-7</td><td class="column-2">23.33</td><td class="column-3">6.74</td><td class="column-4">700</td><td class="column-5">1.25</td><td class="column-6">488</td></tr><tr class="row-15 odd" role="row"><td class="column-1">gzip-8</td><td class="column-2">23.25</td><td class="column-3">9.82</td><td class="column-4">692</td><td class="column-5">1.27</td><td class="column-6">488</td></tr><tr class="row-16 even" role="row"><td class="column-1">gzip-9</td><td class="column-2">23.23</td><td class="column-3">13.2</td><td class="column-4">694</td><td class="column-5">1.25</td><td class="column-6">486</td></tr><tr class="row-17 odd" role="row"><td class="column-1">bzip2-1</td><td class="column-2">21.81</td><td class="column-3">17.5</td><td class="column-4">1 554</td><td class="column-5">4.62</td><td class="column-6">898</td></tr><tr class="row-18 even" role="row"><td class="column-1">bzip2-2</td><td class="column-2">20.59</td><td class="column-3">17.6</td><td class="column-4">2 336</td><td class="column-5">4.48</td><td class="column-6">1 288</td></tr><tr class="row-19 odd" role="row"><td class="column-1">bzip2-3</td><td class="column-2">20.02</td><td class="column-3">17.8</td><td class="column-4">3 120</td><td class="column-5">4.43</td><td class="column-6">1 700</td></tr><tr class="row-20 even" role="row"><td class="column-1">bzip2-4</td><td class="column-2">19.66</td><td class="column-3">18.5</td><td class="column-4">3 900</td><td class="column-5">4.49</td><td class="column-6">3 900</td></tr><tr class="row-21 odd" role="row"><td class="column-1">bzip2-5</td><td class="column-2">19.42</td><td class="column-3">20.0</td><td class="column-4">4 688</td><td class="column-5">4.56</td><td class="column-6">2 468</td></tr></tbody></table>

<table id="tablepress-2" class="tablepress tablepress-id-2 dataTable no-footer" role="grid" aria-describedby="tablepress-2_info"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody class="row-hover"><tr class="row-22 even" role="row"><td class="column-1">bzip2-6</td><td class="column-2">19.25</td><td class="column-3">20.6</td><td class="column-4">5 468</td><td class="column-5">4.76</td><td class="column-6">2 878</td></tr><tr class="row-23 odd" role="row"><td class="column-1">bzip2-7</td><td class="column-2">19.07</td><td class="column-3">21.9</td><td class="column-4">6 256</td><td class="column-5">5.07</td><td class="column-6">3 250</td></tr><tr class="row-24 even" role="row"><td class="column-1">bzip2-8</td><td class="column-2">18.94</td><td class="column-3">22.5</td><td class="column-4">7 040</td><td class="column-5">5.08</td><td class="column-6">3 644</td></tr><tr class="row-25 odd" role="row"><td class="column-1">bzip2-9</td><td class="column-2">18.89</td><td class="column-3">22.6</td><td class="column-4">7 820</td><td class="column-5">5.38</td><td class="column-6">4 040</td></tr><tr class="row-26 even" role="row"><td class="column-1">lzma-0</td><td class="column-2">23.16</td><td class="column-3">10.3</td><td class="column-4">1 980</td><td class="column-5">3.42</td><td class="column-6">840</td></tr><tr class="row-27 odd" role="row"><td class="column-1">lzma-1</td><td class="column-2">21.94</td><td class="column-3">13.1</td><td class="column-4">2 000</td><td class="column-5">3.34</td><td class="column-6">824</td></tr><tr class="row-28 even" role="row"><td class="column-1">lzma-2</td><td class="column-2">20.08</td><td class="column-3">13.1</td><td class="column-4">5 476</td><td class="column-5">3.11</td><td class="column-6">1 272</td></tr><tr class="row-29 odd" role="row"><td class="column-1">lzma-3</td><td class="column-2">17.24</td><td class="column-3">60.3</td><td class="column-4">13 600</td><td class="column-5">2.44</td><td class="column-6">1 788</td></tr><tr class="row-30 even" role="row"><td class="column-1">lzma-4</td><td class="column-2">16.64</td><td class="column-3">66.8</td><td class="column-4">25 376</td><td class="column-5">2.40</td><td class="column-6">2 814</td></tr><tr class="row-31 odd" role="row"><td class="column-1">lzma-5</td><td class="column-2">16.21</td><td class="column-3">69.2</td><td class="column-4">48 926</td><td class="column-5">2.28</td><td class="column-6">4 858</td></tr></tbody></table>

<table id="tablepress-2" class="tablepress tablepress-id-2 dataTable no-footer" role="grid" aria-describedby="tablepress-2_info"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody class="row-hover"><tr class="row-32 even" role="row"><td class="column-1">lzma-6</td><td class="column-2">15.62</td><td class="column-3">90.5</td><td class="column-4">96 030</td><td class="column-5">2.21</td><td class="column-6">8 952</td></tr><tr class="row-33 odd" role="row"><td class="column-1">lzma-7</td><td class="column-2">15.36</td><td class="column-3">97.6</td><td class="column-4">190 260</td><td class="column-5">2.24</td><td class="column-6">17 146</td></tr><tr class="row-34 even" role="row"><td class="column-1">lzma-8</td><td class="column-2">15.17</td><td class="column-3">106</td><td class="column-4">378 688</td><td class="column-5">2.25</td><td class="column-6">33 536</td></tr><tr class="row-35 odd" role="row"><td class="column-1">lzma-9</td><td class="column-2">15.04</td><td class="column-3">113</td><td class="column-4">689 956</td><td class="column-5">2.23</td><td class="column-6">66 304</td></tr><tr class="row-36 even" role="row"><td class="column-1">xz-0</td><td class="column-2">23.16</td><td class="column-3">10.7</td><td class="column-4">2 088</td><td class="column-5">3.63</td><td class="column-6">864</td></tr><tr class="row-37 odd" role="row"><td class="column-1">xz-1</td><td class="column-2">21.95</td><td class="column-3">11.5</td><td class="column-4">2 066</td><td class="column-5">3.31</td><td class="column-6">875</td></tr><tr class="row-38 even" role="row"><td class="column-1">xz-2</td><td class="column-2">20.08</td><td class="column-3">13.2</td><td class="column-4">5 556</td><td class="column-5">2.96</td><td class="column-6">1 300</td></tr><tr class="row-39 odd" role="row"><td class="column-1">xz-3</td><td class="column-2">17.25</td><td class="column-3">63.0</td><td class="column-4">13 684</td><td class="column-5">2.70</td><td class="column-6">1 830</td></tr><tr class="row-40 even" role="row"><td class="column-1">xz-4</td><td class="column-2">16.64</td><td class="column-3">65.6</td><td class="column-4">25 450</td><td class="column-5">2.60</td><td class="column-6">2 836</td></tr><tr class="row-41 odd" role="row"><td class="column-1">xz-5</td><td class="column-2">16.21</td><td class="column-3">70.0</td><td class="column-4">49 012</td><td class="column-5">2.48</td><td class="column-6">4 886</td></tr></tbody></table>

<table id="tablepress-2" class="tablepress tablepress-id-2 dataTable no-footer" role="grid" aria-describedby="tablepress-2_info"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-2" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody class="row-hover"><tr class="row-42 even" role="row"><td class="column-1">xz-6</td><td class="column-2">15.62</td><td class="column-3">90.5</td><td class="column-4">96 112</td><td class="column-5">2.50</td><td class="column-6">9 000</td></tr><tr class="row-43 odd" role="row"><td class="column-1">xz-7</td><td class="column-2">15.36</td><td class="column-3">97.4</td><td class="column-4">190 324</td><td class="column-5">2.40</td><td class="column-6">17 196</td></tr><tr class="row-44 even" role="row"><td class="column-1">xz-8</td><td class="column-2">15.17</td><td class="column-3">110</td><td class="column-4">378 740</td><td class="column-5">2.44</td><td class="column-6">35 556</td></tr><tr class="row-45 odd" role="row"><td class="column-1">xz-9</td><td class="column-2">15.05</td><td class="column-3">117</td><td class="column-4">690 060</td><td class="column-5">2.46</td><td class="column-6">66 326</td></tr></tbody></table>

#### Results analysis

<div id="tablepress-4_wrapper" class="dataTables_wrapper no-footer"><table id="tablepress-4" class="tablepress tablepress-id-4 dataTable no-footer" role="grid"><thead><tr class="row-1 odd" role="row"><th class="column-1 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="algo: activate to sort column ascending" style="width: 77px;">algo</th><th class="column-2 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="size (Mb): activate to sort column ascending" style="width: 79px;">size (Mb)</th><th class="column-3 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="ctime (s): activate to sort column ascending" style="width: 79px;">ctime (s)</th><th class="column-4 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="cmem (Kb): activate to sort column ascending" style="width: 88px;">cmem (Kb)</th><th class="column-5 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="dtime (s): activate to sort column ascending" style="width: 80px;">dtime (s)</th><th class="column-6 sorting" tabindex="0" aria-controls="tablepress-4" rowspan="1" colspan="1" aria-label="dmem (Kb): activate to sort column ascending" style="width: 90px;">dmem (Kb)</th></tr></thead><tbody><tr class="row-2 even" role="row"><td class="column-1">xz-9</td><td class="column-2">15.05</td><td class="column-3">117</td><td class="column-4"><span style="color:darkred; ">690 060</span></td><td class="column-5">2.46</td><td class="column-6"><span style="color:darkred; ">66 326</span></td></tr><tr class="row-3 odd" role="row"><td class="column-1">xz-8</td><td class="column-2">15.17</td><td class="column-3">110</td><td class="column-4"><span style="color:darkred; ">378 740</span></td><td class="column-5">2.44</td><td class="column-6"><span style="color:darkred; ">35 556</span></td></tr><tr class="row-4 even" role="row"><td class="column-1">xz-7</td><td class="column-2">15.36</td><td class="column-3">97.4</td><td class="column-4"><span style="color:darkred; ">190 324</span></td><td class="column-5">2.40</td><td class="column-6"><span style="color:darkred; ">17 196</span></td></tr><tr class="row-5 odd" role="row"><td class="column-1">xz-6</td><td class="column-2">15.62</td><td class="column-3">90.5</td><td class="column-4"><span style="color:darkred; ">96 112</span></td><td class="column-5">2.50</td><td class="column-6">9 000</td></tr><tr class="row-6 even" role="row"><td class="column-1">xz-5</td><td class="column-2">16.21</td><td class="column-3">70.0</td><td class="column-4"><span style="color:darkred; ">49 012</span></td><td class="column-5">2.48</td><td class="column-6">4 886</td></tr><tr class="row-7 odd" role="row"><td class="column-1">xz-4</td><td class="column-2">16.64</td><td class="column-3">65.6</td><td class="column-4"><span style="color:darkred; ">25 450</span></td><td class="column-5">2.60</td><td class="column-6">2 836</td></tr><tr class="row-8 even" role="row"><td class="column-1">xz-3</td><td class="column-2">17.25</td><td class="column-3"><span style="color:darkred; ">63.0</span></td><td class="column-4">13 684</td><td class="column-5">2.70</td><td class="column-6">1 830</td></tr><tr class="row-9 odd" role="row"><td class="column-1">bzip2-9</td><td class="column-2">18.89</td><td class="column-3"><span style="color:darkred; ">22.6</span></td><td class="column-4">7 820</td><td class="column-5">5.38</td><td class="column-6">4 040</td></tr><tr class="row-10 even" role="row"><td class="column-1">bzip2-8</td><td class="column-2">18.94</td><td class="column-3">22.5</td><td class="column-4">7 040</td><td class="column-5">5.08</td><td class="column-6">3 644</td></tr><tr class="row-11 odd" role="row"><td class="column-1">bzip2-7</td><td class="column-2">19.07</td><td class="column-3">21.9</td><td class="column-4">6 256</td><td class="column-5">5.07</td><td class="column-6">3 250</td></tr><tr class="row-12 even" role="row"><td class="column-1">bzip2-6</td><td class="column-2">19.25</td><td class="column-3">20.6</td><td class="column-4">5 468</td><td class="column-5">4.76</td><td class="column-6">2 878</td></tr><tr class="row-13 odd" role="row"><td class="column-1">bzip2-5</td><td class="column-2">19.42</td><td class="column-3">20.0</td><td class="column-4">4 688</td><td class="column-5">4.56</td><td class="column-6">2 468</td></tr><tr class="row-14 even" role="row"><td class="column-1">bzip2-4</td><td class="column-2">19.66</td><td class="column-3">18.5</td><td class="column-4">3 900</td><td class="column-5">4.49</td><td class="column-6">3 900</td></tr><tr class="row-15 odd" role="row"><td class="column-1">bzip2-3</td><td class="column-2">20.02</td><td class="column-3">17.8</td><td class="column-4">3 120</td><td class="column-5">4.43</td><td class="column-6">1 700</td></tr><tr class="row-16 even" role="row"><td class="column-1">xz-2</td><td class="column-2">20.08</td><td class="column-3">13.2</td><td class="column-4">5 556</td><td class="column-5">2.96</td><td class="column-6">1 300</td></tr><tr class="row-17 odd" role="row"><td class="column-1"><span style="color:grey; ">bzip2-2</span></td><td class="column-2"><span style="color:grey; ">20.59</span></td><td class="column-3"><span style="color:grey; ">17.6</span></td><td class="column-4"><span style="color:grey; ">2 336</span></td><td class="column-5"><span style="color:grey; ">4.48</span></td><td class="column-6"><span style="color:grey; ">1 288</span></td></tr><tr class="row-18 even" role="row"><td class="column-1"><span style="color:grey; ">bzip2-1</span></td><td class="column-2"><span style="color:grey; ">21.81</span></td><td class="column-3"><span style="color:grey; ">17.5</span></td><td class="column-4"><span style="color:grey; ">1 554</span></td><td class="column-5"><span style="color:grey; ">4.62</span></td><td class="column-6"><span style="color:grey; ">898</span></td></tr><tr class="row-19 odd" role="row"><td class="column-1">xz-1</td><td class="column-2">21.95</td><td class="column-3">11.5</td><td class="column-4">2 066</td><td class="column-5">3.31</td><td class="column-6">875</td></tr><tr class="row-20 even" role="row"><td class="column-1">xz-0</td><td class="column-2">23.16</td><td class="column-3">10.7</td><td class="column-4">2 088</td><td class="column-5">3.63</td><td class="column-6">864</td></tr><tr class="row-21 odd" role="row"><td class="column-1"><span style="color:grey; ">gzip-9</span></td><td class="column-2"><span style="color:grey; ">23.23</span></td><td class="column-3"><span style="color:grey; ">13.2</span></td><td class="column-4"><span style="color:grey; ">694</span></td><td class="column-5"><span style="color:grey; ">1.25</span></td><td class="column-6"><span style="color:grey; ">486</span></td></tr><tr class="row-22 even" role="row"><td class="column-1">gzip-8</td><td class="column-2">23.25</td><td class="column-3">9.82</td><td class="column-4">692</td><td class="column-5">1.27</td><td class="column-6">488</td></tr><tr class="row-23 odd" role="row"><td class="column-1">gzip-7</td><td class="column-2">23.33</td><td class="column-3">6.74</td><td class="column-4">700</td><td class="column-5">1.25</td><td class="column-6">488</td></tr><tr class="row-24 even" role="row"><td class="column-1">gzip-6</td><td class="column-2">23.43</td><td class="column-3">5.78</td><td class="column-4">716</td><td class="column-5">1.29</td><td class="column-6">488</td></tr><tr class="row-25 odd" role="row"><td class="column-1">gzip-5</td><td class="column-2">23.82</td><td class="column-3">4.43</td><td class="column-4">718</td><td class="column-5">1.27</td><td class="column-6">500</td></tr><tr class="row-26 even" role="row"><td class="column-1">gzip-4</td><td class="column-2">24.77</td><td class="column-3">3.56</td><td class="column-4">708</td><td class="column-5">1.33</td><td class="column-6">486</td></tr><tr class="row-27 odd" role="row"><td class="column-1">gzip-3</td><td class="column-2">26.50</td><td class="column-3">3.22</td><td class="column-4">708</td><td class="column-5">1.40</td><td class="column-6">484</td></tr><tr class="row-28 even" role="row"><td class="column-1"><span style="color:grey; ">lzop-9</span></td><td class="column-2"><span style="color:grey; ">26.73</span></td><td class="column-3"><span style="color:grey; ">33.3</span></td><td class="column-4"><span style="color:grey; ">1 308</span></td><td class="column-5"><span style="color:grey; ">0.60</span></td><td class="column-6"><span style="color:grey; ">?</span></td></tr><tr class="row-29 odd" role="row"><td class="column-1"><span style="color:grey; ">lzop-8</span></td><td class="column-2"><span style="color:grey; ">26.74</span></td><td class="column-3"><span style="color:grey; ">27.67</span></td><td class="column-4"><span style="color:grey; ">1 308</span></td><td class="column-5"><span style="color:grey; ">0.65</span></td><td class="column-6"><span style="color:grey; ">?</span></td></tr><tr class="row-30 even" role="row"><td class="column-1"><span style="color:grey; ">lzop-7</span></td><td class="column-2"><span style="color:grey; ">27.07</span></td><td class="column-3"><span style="color:grey; ">13.15</span></td><td class="column-4"><span style="color:grey; ">1 312</span></td><td class="column-5"><span style="color:grey; ">0.70</span></td><td class="column-6"><span style="color:grey; ">?</span></td></tr><tr class="row-31 odd" role="row"><td class="column-1">gzip-2</td><td class="column-2">27.44</td><td class="column-3">2.90</td><td class="column-4">708</td><td class="column-5">1.42</td><td class="column-6">486</td></tr><tr class="row-32 even" role="row"><td class="column-1">gzip-1</td><td class="column-2"><span style="color:darkred; ">28.72</span></td><td class="column-3">2.74</td><td class="column-4">708</td><td class="column-5">1.42</td><td class="column-6">486</td></tr><tr class="row-33 odd" role="row"><td class="column-1">lzop-1</td><td class="column-2"><span style="color:darkred; ">36.17</span></td><td class="column-3">1.04</td><td class="column-4">1 004</td><td class="column-5">0.63</td><td class="column-6">?</td></tr><tr class="row-34 even" role="row"><td class="column-1"><span style="color:grey; ">lzop-3</span></td><td class="column-2"><span style="color:grey; ">36.38</span></td><td class="column-3"><span style="color:grey; ">1.11</span></td><td class="column-4"><span style="color:grey; ">940</span></td><td class="column-5"><span style="color:grey; ">0.65</span></td><td class="column-6"><span style="color:grey; ">?</span></td></tr><tr class="row-35 odd" role="row"><td class="column-1"><span style="color:grey; ">compress</span></td><td class="column-2"><span style="color:grey; ">39.56</span></td><td class="column-3"><span style="color:grey; ">2.64</span></td><td class="column-4"><span style="color:grey; ">1 124</span></td><td class="column-5"><span style="color:grey; ">1.60</span></td><td class="column-6"><span style="color:grey; ">548</span></td></tr></tbody></table></div>