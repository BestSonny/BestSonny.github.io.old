---
layout: page
##title: CTPN
permalink: /project/CTPN/
---

     
<div class="section head">
	<center><h1> Detecting Text in Natural Image with Connectionist Text Proposal Network </h1>
	<div class="authors">
	  <a href="">Zhi Tian,</a>&nbsp;&nbsp;
	  <a href="http://www.wlhuang.com/">Weilin Huang,</a>&nbsp;&nbsp;
	  <a href="">Tong He,</a>&nbsp;&nbsp;
	  <a href="http://bestsonny.github.io/" >Pan He,</a>&nbsp;&nbsp;
	  <a href="http://mmlab.siat.ac.cn/yuqiao/" >Yu Qiao,</a>&nbsp;&nbsp;
	</div>

	<div class="affiliations">
	  <a href="">Shenzhen Key Lab of Comp. Vis and Pat. Rec.,</a>
	  <a href="http://english.siat.cas.cn/"> Shenzhen Institutes of Advanced Technology, </a>
	  <a href="http://english.cas.cn/">Chinese Academy of Sciences</a>
	</div>
	
        <div class="affiliations">
	  <a href="http://www.ox.ac.uk/">University of Oxford</a>
	</div>

	<div class="affiliations">
	  <a href="http://mmlab.ie.cuhk.edu.hk/">Multimedia Laboratory, </a>
	  <a href="http://www.ie.cuhk.edu.hk/">Department of Information Engineering, </a>
	  <a href="http://www.cuhk.edu.hk">The Chinese University of Hong Kong</a>
	</div>


	<div class="venue">European Conference on Computer Vision (<a href="http://www.eccv2016.org/" target="_blank">ECCV</a>) 2016, Amsterdam, The Netherlands
	</div>
	<br>

    </center><center><img src="/images/ctpn_eccv2016.png" border="0" width="85%"></center>
</div>


<div style="text-align: justify" class="section abstract">

	<h2>Abstract</h2>
	<p>We propose a novel Connectionist Text Proposal Network (CTPN) that accurately localizes text lines in natural image. The CTPN detects a text line in a sequence of fine-scale text proposals directly
in convolutional feature maps. We develop a vertical anchor mechanism that jointly predicts location and text/non-text score of each fixed-width proposal, considerably improving localization accuracy. The sequential
proposals are naturally connected by a recurrent neural network, which is seamlessly incorporated into the convolutional network, resulting in an end-to-end trainable model. This allows the CTPN to explore rich context information of image, making it powerful to detect extremely
ambiguous text. The CTPN works reliably on multi-scale and multilanguage text without further post-processing, departing from previous bottom-up methods requiring multi-step post filtering. It achieves 0.88
and 0.61 F-measure on the ICDAR 2013 and 2015 benchmarks, surpassing recent results by a large margin. The CTPN is computationally efficient with 0.14s/image, by using the very deep VGG16 model [27]. Online demo is available at: http://textdet.com/.
	</p>
</div>

<div class="section list">
	<h2>Citation</h2>
	
	<div class="section bibtex">
	  <pre>@inproceedings{zhitian16detectingtext,
 Author    = {Zhi Tian and
              Weilin Huang and
	      Tong He and
	      Pan He and
              Yu Qiao},
 Title     = {Detecting Text in Natural Image with Connectionist Text Proposal Network},
 Booktitle = {in Proceedings of European Conference on Computer Vision, (ECCV)},
 Year      = {2016}}
	</pre>
	</div>
</div>








