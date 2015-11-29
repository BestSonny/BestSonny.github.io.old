---
layout: page
##title: DTRN
permalink: /project/DTRN/
---

     
<div class="section head">
	<center><h1> Reading Scene Text in Deep Convolutional Sequences </h1>
	<div class="authors">
	  <a href="http://bestsonny.github.io/">Pan He,</a>&nbsp;&nbsp;
	  <a href="http://www.wlhuang.com/">Weilin Huang,</a>&nbsp;&nbsp;
	  <a href="http://mmlab.siat.ac.cn/yuqiao/" >Yu Qiao,</a>&nbsp;&nbsp;
	  <a href="http://personal.ie.cuhk.edu.hk/~ccloy/" >Chen Change Loy,</a>&nbsp;&nbsp;
	  <a href="http://www.ie.cuhk.edu.hk/people/xotang.shtml">Xiaoou Tang</a>
	</div>

	<div class="affiliations">
	  <a href="">Shenzhen Key Lab of Comp. Vis and Pat. Rec.,</a>
	  <a href="http://english.siat.cas.cn/"> Shenzhen Institutes of Advanced Technology, </a>
	  <a href="http://english.cas.cn/">Chinese Academy of Sciences</a>
	</div>
	
	<div class="affiliations">
	  <a href="http://mmlab.ie.cuhk.edu.hk/">Multimedia Laboratory, </a>
	  <a href="http://www.ie.cuhk.edu.hk/">Department of Information Engineering, </a>
	  <a href="www.cuhk.edu.hk">The Chinese University of Hong Kong</a>
	</div>


	<div class="venue">AAAI Conference on Artificial Intelligence (<a href="http://www.aaai.org/Conferences/AAAI/aaai16.php" target="_blank">AAAI</a>) 2016, Phoenix, Arizona USA
	</div>
	<br>

    </center><center><img src="/images/project.png" border="0" width="85%"></center>
</div>


<div style="text-align: justify" class="section abstract">

	<h2>Abstract</h2>
	<p>
	We develop a Deep-Text Recurrent Network (DTRN) that regards scene text reading as a sequence labelling problem. We leverage recent advances of deep convolutional neural networks to generate an ordered high-level sequence from a whole word image, avoiding the difficult character segmentation problem. Then a deep recurrent model, building on long short-term memory (LSTM), is developed to robustly recognize the generated CNN sequences, departing from most existing approaches recognising each character independently. Our model has a number of appealing properties in comparison to existing scene text recognition methods: (i) It can recognise highly ambiguous words by leveraging meaningful context information, allowing it to work reliably without either pre- or post-processing; (ii) the deep CNN feature is robust to various image distortions; (iii) it retains the explicit order information in word image, which is essential to discriminate word strings; (iv) the model does not depend on pre-defined dictionary, and it can process unknown words and arbitrary strings. It achieves impressive results on several benchmarks, advancing the-state-of-the-art substantially.	
	</p>
</div>


<div class="section list">
	<h2>Citation</h2>
	
	<div class="section bibtex">
	  <pre>@inproceedings{panhe16readText,
 Author    = {Pan He and
              Weilin Huang and
              Yu Qiao and
              Chen Change Loy and 
              Xiaoou Tang},
 Title     = {Reading Scene Text in Deep Convolutional Sequences},
 Booktitle = {in Proceedings of AAAI Conference on Artificial Intelligence, (AAAI)},
 Year      = {2016}}
	</pre>
	</div>
</div>





