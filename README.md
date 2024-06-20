# Stock-volatility-prediction-based-on-multiple-LSTM-models
## Introduction
Stock volatility can reflect the volatility of the price and the future risk of the assets, and historical volatility is an important measure of stock volatility. The scientific and accurate prediction model of stock historical volatility is of great significance for the estimation of the future asset risk situation and the maintenance of the smooth operation of the financial market. Classical time series models have been widely used. <br>In order to obtain more accurate prediction models, this report proposes the stock historical volatility prediction model composed of *`two LSTM neural networks and two fully connected layers`*, so as to improve the ability of the model to effectively capture the complex nonlinear relationship in the time series prediction task.
## Core Model
### LSTM model of two fully connected layers
The neural network structure we take consists of two fully connected layers and two LSTM layers. In order to accelerate the convergence speed, enhance the model stability, and improve the generalization ability, we add the batch standardization (BN) layer before the LSTM network of each layer. To improve the ability of the model to express non-linear sequences, we added the full connection (Dense) layer before and at the end of the LSTM network. The specific structure of the model is as follows:<br><br><br>
.<div align=center>
![图片1](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/fa903923-8004-4732-8e4a-b1daebfe0a23)
</div>
## Model Prediction
After model training, we predicted the historical stock volatility of the next ten time steps according to the model parameters, and then rever-normalized the predicted value of the features to get the predicted result. The prediction data and effect of the model are shown as follows:<br><br><br>
<table class="MsoTableGrid" border="1" cellspacing="0" style="border-collapse:collapse;width:482.1500pt;margin-left:-41.5500pt;
border:none;mso-border-left-alt:0.5000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;
mso-border-right-alt:0.5000pt solid windowtext;mso-border-bottom-alt:0.5000pt solid windowtext;mso-border-insideh:0.5000pt solid windowtext;
mso-border-insidev:0.5000pt solid windowtext;mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;"><tbody><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">时间步</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">1</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">2</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">3</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">4</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">5</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">6</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">7</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">8</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">9</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">10</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">预测值</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">394</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.01</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">3359</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">13317</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">139</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12879</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12583</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12271</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">11974</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.012950</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">11705</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">实际值</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013124</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013173</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013323</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013156</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.012638</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013058</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013418</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013200</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013227</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.009707</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr></tbody></table>

<br><br><br>
.<div align=center>
![图片2](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/bb6e35b1-f116-4664-9c85-5627d989552b)
</div>
## Model Comparison 
To analyze the predictive performance of this Model (hereinafter referred to as Model), we compared the model with the ARIMA model, and the model with only one hidden layer node number of 26 LSTM layer and fully Dense layer (hereinafter referred to as Baseline) for the next ten time steps. Among them, the training process of the neural network model used as a comparison is consistent with the above training process, and the model parameters are saved in the file "baseline.h5". The historical volatility data of the next ten time steps are still calculated from the daily frequency stock quote data of Eastern Wealth climbed by akshare.<br><br>
We visually compared the prediction results of the three models, and used four indicators, namely MSE (mean square error), RMSE (root mean square error), NMSE (standardized mean square error) and MAE (mean absolute error), to conduct quantitative analysis of the prediction performance of the three models. The analysis results are as follows:
<br><br><br>
.<div align=center>
  
![图片1](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/0c67c0b9-350c-44d4-8fcf-a196d4bbe731)
</div>
## Conclusion
It can be seen that, under the evaluation criteria of the four indicators, the prediction performance of Model Model is higher than that of ARIMA model, and the prediction performance of LSTM model for historical volatility is significantly higher than that of ARIMA model, and model has the best prediction performance. In addition, we can see from the image that the predicted value of the ARIMA Model fluctuates very little, while the Baseline and model have a clear trend, which indicates that `the LSTM model is more likely than the ARIMA model to capture small fluctuations when the data is relatively small, has higher sensitivity to the data, and can better deal with complex time series patterns and long-term trends`.
## Bibliography
[1]Lei, L., Yu, J., Wei, Y., & Lai, X. (2018), “Economic policy uncertainty and China's stock market volatility forecasting research,” Management Science, 21(06), 88-98.<br>
[2] Wei, Y. (2010), “ Research on the optimal volatility forecasting model for China's stock market - An empirical analysis based on high-frequency data of the Shanghai and Shenzhen 300 Index,” Management Tribune, 7(06), 936-942.<br>
[3] Zhang, T., Yuan, Y., & Zeng, W. (2020), “Can investor attention improve market volatility prediction accuracy? - An empirical study based on high-frequency data of China's stock market,” Chinese Management Science, 28(11), 192-205.<br>
[4] Yan, D., & Li, Y. (2008), “Volatility forecasting of the Shanghai and Shenzhen 300 index based on GARCH models,” Journal of Lanzhou Jiaotong University, (01), 92-95.<br>
[5] Shi, X. Y. (2022), “Research on the volatility prediction of the stock market based on the improved EEMD-LSTM-Adaboost combination model,” (Doctoral dissertation, Shanghai Normal University). https://doi.org/10.27312/d.cnki.gshsu.2022.000748<br>
[6] Zhang, H. (2020), “A short-term stock volatility prediction method based on deep learning,” Modern Marketing (Business Edition), (05), 179-181.<br>
[7] Deng, G. X. (2024), “Research on stock market volatility prediction based on EEMD-LSTM,” (Doctoral dissertation, Southwestern University of Finance and Economics).
