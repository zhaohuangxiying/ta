var isIE5 = !! navigator.userAgent.match(/MSIE 5.0/);
var isIE6 = !! navigator.userAgent.match(/MSIE 6.0/);
var isIE7 = !! navigator.userAgent.match(/MSIE 7.0/);
var isIE8 = !! navigator.userAgent.match(/MSIE 8.0/);
var isIE9 = !! navigator.userAgent.match(/MSIE 9.0/);
var isIE10 = !! navigator.userAgent.match(/MSIE 10.0/);
var isChrome = !! navigator.userAgent.match(/Chrome/);

window.mediaID = 0;

/* Bootstrap v3.3.4 (http://getbootstrap.com) * Copyright 2011-2015 Twitter, Inc. * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE) */
if("undefined"==typeof jQuery)throw new Error("Bootstrap's JavaScript requires jQuery");+function(t){"use strict";var e=t.fn.jquery.split(" ")[0].split(".");if(e[0]<2&&e[1]<9||1==e[0]&&9==e[1]&&e[2]<1)throw new Error("Bootstrap's JavaScript requires jQuery version 1.9.1 or higher")}(jQuery),+function(t){"use strict";function e(e){return this.each(function(){var o=t(this),n=o.data("bs.button"),s="object"==typeof e&&e;n||o.data("bs.button",n=new i(this,s)),"toggle"==e?n.toggle():e&&n.setState(e)})}var i=function(e,o){this.$element=t(e),this.options=t.extend({},i.DEFAULTS,o),this.isLoading=!1};i.VERSION="3.3.2",i.DEFAULTS={loadingText:"loading..."},i.prototype.setState=function(e){var i="disabled",o=this.$element,n=o.is("input")?"val":"html",s=o.data();e+="Text",null==s.resetText&&o.data("resetText",o[n]()),setTimeout(t.proxy(function(){o[n](null==s[e]?this.options[e]:s[e]),"loadingText"==e?(this.isLoading=!0,o.addClass(i).attr(i,i)):this.isLoading&&(this.isLoading=!1,o.removeClass(i).removeAttr(i))},this),0)},i.prototype.toggle=function(){var t=!0,e=this.$element.closest('[data-toggle="buttons"]');if(e.length){var i=this.$element.find("input");"radio"==i.prop("type")&&(i.prop("checked")&&this.$element.hasClass("active")?t=!1:e.find(".active").removeClass("active")),t&&i.prop("checked",!this.$element.hasClass("active")).trigger("change")}else this.$element.attr("aria-pressed",!this.$element.hasClass("active"));t&&this.$element.toggleClass("active")};var o=t.fn.button;t.fn.button=e,t.fn.button.Constructor=i,t.fn.button.noConflict=function(){return t.fn.button=o,this},t(document).on("click.bs.button.data-api",'[data-toggle^="button"]',function(i){var o=t(i.target);o.hasClass("btn")||(o=o.closest(".btn")),e.call(o,"toggle"),i.preventDefault()}).on("focus.bs.button.data-api blur.bs.button.data-api",'[data-toggle^="button"]',function(e){t(e.target).closest(".btn").toggleClass("focus",/^focus(in)?$/.test(e.type))})}(jQuery),+function(t){"use strict";function e(e){e&&3===e.which||(t(n).remove(),t(s).each(function(){var o=t(this),n=i(o),s={relatedTarget:this};n.hasClass("open")&&(n.trigger(e=t.Event("hide.bs.dropdown",s)),e.isDefaultPrevented()||(o.attr("aria-expanded","false"),n.removeClass("open").trigger("hidden.bs.dropdown",s)))}))}function i(e){var i=e.attr("data-target");i||(i=e.attr("href"),i=i&&/#[A-Za-z]/.test(i)&&i.replace(/.*(?=#[^\s]*$)/,""));var o=i&&t(i);return o&&o.length?o:e.parent()}function o(e){return this.each(function(){var i=t(this),o=i.data("bs.dropdown");o||i.data("bs.dropdown",o=new r(this)),"string"==typeof e&&o[e].call(i)})}var n=".dropdown-backdrop",s='[data-toggle="dropdown"]',r=function(e){t(e).on("click.bs.dropdown",this.toggle)};r.VERSION="3.3.2",r.prototype.toggle=function(o){var n=t(this);if(!n.is(".disabled, :disabled")){var s=i(n),r=s.hasClass("open");if(e(),!r){"ontouchstart"in document.documentElement&&!s.closest(".navbar-nav").length&&t('<div class="dropdown-backdrop"/>').insertAfter(t(this)).on("click",e);var a={relatedTarget:this};if(s.trigger(o=t.Event("show.bs.dropdown",a)),o.isDefaultPrevented())return;n.trigger("focus").attr("aria-expanded","true"),s.toggleClass("open").trigger("shown.bs.dropdown",a)}return!1}},r.prototype.keydown=function(e){if(/(38|40|27|32)/.test(e.which)&&!/input|textarea/i.test(e.target.tagName)){var o=t(this);if(e.preventDefault(),e.stopPropagation(),!o.is(".disabled, :disabled")){var n=i(o),r=n.hasClass("open");if(!r&&27!=e.which||r&&27==e.which)return 27==e.which&&n.find(s).trigger("focus"),o.trigger("click");var a=" li:not(.disabled):visible a",l=n.find('[role="menu"]'+a+', [role="listbox"]'+a);if(l.length){var h=l.index(e.target);38==e.which&&h>0&&h--,40==e.which&&h<l.length-1&&h++,~h||(h=0),l.eq(h).trigger("focus")}}}};var a=t.fn.dropdown;t.fn.dropdown=o,t.fn.dropdown.Constructor=r,t.fn.dropdown.noConflict=function(){return t.fn.dropdown=a,this},t(document).on("click.bs.dropdown.data-api",e).on("click.bs.dropdown.data-api",".dropdown form",function(t){t.stopPropagation()}).on("click.bs.dropdown.data-api",s,r.prototype.toggle).on("keydown.bs.dropdown.data-api",s,r.prototype.keydown).on("keydown.bs.dropdown.data-api",'[role="menu"]',r.prototype.keydown).on("keydown.bs.dropdown.data-api",'[role="listbox"]',r.prototype.keydown)}(jQuery),+function(t){"use strict";function e(e){return this.each(function(){var o=t(this),n=o.data("bs.tooltip"),s="object"==typeof e&&e;(n||!/destroy|hide/.test(e))&&(n||o.data("bs.tooltip",n=new i(this,s)),"string"==typeof e&&n[e]())})}var i=function(t,e){this.type=null,this.options=null,this.enabled=null,this.timeout=null,this.hoverState=null,this.$element=null,this.init("tooltip",t,e)};i.VERSION="3.3.2",i.TRANSITION_DURATION=150,i.DEFAULTS={animation:!0,placement:"top",selector:!1,template:'<div class="tooltip" role="tooltip"><div class="tooltip-arrow"></div><div class="tooltip-inner"></div></div>',trigger:"hover focus",title:"",delay:0,html:!1,container:!1,viewport:{selector:"body",padding:0}},i.prototype.init=function(e,i,o){if(this.enabled=!0,this.type=e,this.$element=t(i),this.options=this.getOptions(o),this.$viewport=this.options.viewport&&t(this.options.viewport.selector||this.options.viewport),this.$element[0]instanceof document.constructor&&!this.options.selector)throw new Error("`selector` option must be specified when initializing "+this.type+" on the window.document object!");for(var n=this.options.trigger.split(" "),s=n.length;s--;){var r=n[s];if("click"==r)this.$element.on("click."+this.type,this.options.selector,t.proxy(this.toggle,this));else if("manual"!=r){var a="hover"==r?"mouseenter":"focusin",l="hover"==r?"mouseleave":"focusout";this.$element.on(a+"."+this.type,this.options.selector,t.proxy(this.enter,this)),this.$element.on(l+"."+this.type,this.options.selector,t.proxy(this.leave,this))}}this.options.selector?this._options=t.extend({},this.options,{trigger:"manual",selector:""}):this.fixTitle()},i.prototype.getDefaults=function(){return i.DEFAULTS},i.prototype.getOptions=function(e){return e=t.extend({},this.getDefaults(),this.$element.data(),e),e.delay&&"number"==typeof e.delay&&(e.delay={show:e.delay,hide:e.delay}),e},i.prototype.getDelegateOptions=function(){var e={},i=this.getDefaults();return this._options&&t.each(this._options,function(t,o){i[t]!=o&&(e[t]=o)}),e},i.prototype.enter=function(e){var i=e instanceof this.constructor?e:t(e.currentTarget).data("bs."+this.type);return i&&i.$tip&&i.$tip.is(":visible")?void(i.hoverState="in"):(i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i)),clearTimeout(i.timeout),i.hoverState="in",i.options.delay&&i.options.delay.show?void(i.timeout=setTimeout(function(){"in"==i.hoverState&&i.show()},i.options.delay.show)):i.show())},i.prototype.leave=function(e){var i=e instanceof this.constructor?e:t(e.currentTarget).data("bs."+this.type);return i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i)),clearTimeout(i.timeout),i.hoverState="out",i.options.delay&&i.options.delay.hide?void(i.timeout=setTimeout(function(){"out"==i.hoverState&&i.hide()},i.options.delay.hide)):i.hide()},i.prototype.show=function(){var e=t.Event("show.bs."+this.type);if(this.hasContent()&&this.enabled){this.$element.trigger(e);var o=t.contains(this.$element[0].ownerDocument.documentElement,this.$element[0]);if(e.isDefaultPrevented()||!o)return;var n=this,s=this.tip(),r=this.getUID(this.type);this.setContent(),s.attr("id",r),this.$element.attr("aria-describedby",r),this.options.animation&&s.addClass("fade");var a="function"==typeof this.options.placement?this.options.placement.call(this,s[0],this.$element[0]):this.options.placement,l=/\s?auto?\s?/i,h=l.test(a);h&&(a=a.replace(l,"")||"top"),s.detach().css({top:0,left:0,display:"block"}).addClass(a).data("bs."+this.type,this),this.options.container?s.appendTo(this.options.container):s.insertAfter(this.$element);var p=this.getPosition(),d=s[0].offsetWidth,c=s[0].offsetHeight;if(h){var f=a,u=this.options.container?t(this.options.container):this.$element.parent(),g=this.getPosition(u);a="bottom"==a&&p.bottom+c>g.bottom?"top":"top"==a&&p.top-c<g.top?"bottom":"right"==a&&p.right+d>g.width?"left":"left"==a&&p.left-d<g.left?"right":a,s.removeClass(f).addClass(a)}var v=this.getCalculatedOffset(a,p,d,c);this.applyPlacement(v,a);var m=function(){var t=n.hoverState;n.$element.trigger("shown.bs."+n.type),n.hoverState=null,"out"==t&&n.leave(n)};t.support.transition&&this.$tip.hasClass("fade")?s.one("bsTransitionEnd",m).emulateTransitionEnd(i.TRANSITION_DURATION):m()}},i.prototype.applyPlacement=function(e,i){var o=this.tip(),n=o[0].offsetWidth,s=o[0].offsetHeight,r=parseInt(o.css("margin-top"),10),a=parseInt(o.css("margin-left"),10);isNaN(r)&&(r=0),isNaN(a)&&(a=0),e.top=e.top+r,e.left=e.left+a,t.offset.setOffset(o[0],t.extend({using:function(t){o.css({top:Math.round(t.top),left:Math.round(t.left)})}},e),0),o.addClass("in");var l=o[0].offsetWidth,h=o[0].offsetHeight;"top"==i&&h!=s&&(e.top=e.top+s-h);var p=this.getViewportAdjustedDelta(i,e,l,h);p.left?e.left+=p.left:e.top+=p.top;var d=/top|bottom/.test(i),c=d?2*p.left-n+l:2*p.top-s+h,f=d?"offsetWidth":"offsetHeight";o.offset(e),this.replaceArrow(c,o[0][f],d)},i.prototype.replaceArrow=function(t,e,i){this.arrow().css(i?"left":"top",50*(1-t/e)+"%").css(i?"top":"left","")},i.prototype.setContent=function(){var t=this.tip(),e=this.getTitle();t.find(".tooltip-inner")[this.options.html?"html":"text"](e),t.removeClass("fade in top bottom left right")},i.prototype.hide=function(e){function o(){"in"!=n.hoverState&&s.detach(),n.$element.removeAttr("aria-describedby").trigger("hidden.bs."+n.type),e&&e()}var n=this,s=t(this.$tip),r=t.Event("hide.bs."+this.type);return this.$element.trigger(r),r.isDefaultPrevented()?void 0:(s.removeClass("in"),t.support.transition&&s.hasClass("fade")?s.one("bsTransitionEnd",o).emulateTransitionEnd(i.TRANSITION_DURATION):o(),this.hoverState=null,this)},i.prototype.fixTitle=function(){var t=this.$element;(t.attr("title")||"string"!=typeof t.attr("data-original-title"))&&t.attr("data-original-title",t.attr("title")||"").attr("title","")},i.prototype.hasContent=function(){return this.getTitle()},i.prototype.getPosition=function(e){e=e||this.$element;var i=e[0],o="BODY"==i.tagName,n=i.getBoundingClientRect();null==n.width&&(n=t.extend({},n,{width:n.right-n.left,height:n.bottom-n.top}));var s=o?{top:0,left:0}:e.offset(),r={scroll:o?document.documentElement.scrollTop||document.body.scrollTop:e.scrollTop()},a=o?{width:t(window).width(),height:t(window).height()}:null;return t.extend({},n,r,a,s)},i.prototype.getCalculatedOffset=function(t,e,i,o){return"bottom"==t?{top:e.top+e.height,left:e.left+e.width/2-i/2}:"top"==t?{top:e.top-o,left:e.left+e.width/2-i/2}:"left"==t?{top:e.top+e.height/2-o/2,left:e.left-i}:{top:e.top+e.height/2-o/2,left:e.left+e.width}},i.prototype.getViewportAdjustedDelta=function(t,e,i,o){var n={top:0,left:0};if(!this.$viewport)return n;var s=this.options.viewport&&this.options.viewport.padding||0,r=this.getPosition(this.$viewport);if(/right|left/.test(t)){var a=e.top-s-r.scroll,l=e.top+s-r.scroll+o;a<r.top?n.top=r.top-a:l>r.top+r.height&&(n.top=r.top+r.height-l)}else{var h=e.left-s,p=e.left+s+i;h<r.left?n.left=r.left-h:p>r.width&&(n.left=r.left+r.width-p)}return n},i.prototype.getTitle=function(){var t,e=this.$element,i=this.options;return t=e.attr("data-original-title")||("function"==typeof i.title?i.title.call(e[0]):i.title)},i.prototype.getUID=function(t){do t+=~~(1e6*Math.random());while(document.getElementById(t));return t},i.prototype.tip=function(){return this.$tip=this.$tip||t(this.options.template)},i.prototype.arrow=function(){return this.$arrow=this.$arrow||this.tip().find(".tooltip-arrow")},i.prototype.enable=function(){this.enabled=!0},i.prototype.disable=function(){this.enabled=!1},i.prototype.toggleEnabled=function(){this.enabled=!this.enabled},i.prototype.toggle=function(e){var i=this;e&&(i=t(e.currentTarget).data("bs."+this.type),i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i))),i.tip().hasClass("in")?i.leave(i):i.enter(i)},i.prototype.destroy=function(){var t=this;clearTimeout(this.timeout),this.hide(function(){t.$element.off("."+t.type).removeData("bs."+t.type)})};var o=t.fn.tooltip;t.fn.tooltip=e,t.fn.tooltip.Constructor=i,t.fn.tooltip.noConflict=function(){return t.fn.tooltip=o,this}}(jQuery);

/*QRCode for JavaScript Copyright (c) 2009 Kazuhiko Arase URL: http://www.d-project.com/ Licensed under the MIT license: http://www.opensource.org/licenses/mit-license.phpThe word "QR Code" is registered trademark of DENSO WAVE INCORPORATED http://www.denso-wave.com/qrcode/faqpatent-e.html*/
function QR8bitByte(data){this.mode=QRMode.MODE_8BIT_BYTE;this.data=data}QR8bitByte.prototype={getLength:function(buffer){return this.data.length},write:function(buffer){for(var i=0;i<this.data.length;i++){buffer.put(this.data.charCodeAt(i),8)}}};function QRCode(typeNumber,errorCorrectLevel){this.typeNumber=typeNumber;this.errorCorrectLevel=errorCorrectLevel;this.modules=null;this.moduleCount=0;this.dataCache=null;this.dataList=new Array()}QRCode.prototype={addData:function(data){var newData=new QR8bitByte(data);this.dataList.push(newData);this.dataCache=null},isDark:function(row,col){if(row<0||this.moduleCount<=row||col<0||this.moduleCount<=col){throw new Error(row+","+col)}return this.modules[row][col]},getModuleCount:function(){return this.moduleCount},make:function(){if(this.typeNumber<1){var typeNumber=1;for(typeNumber=1;typeNumber<40;typeNumber++){var rsBlocks=QRRSBlock.getRSBlocks(typeNumber,this.errorCorrectLevel);var buffer=new QRBitBuffer();var totalDataCount=0;for(var i=0;i<rsBlocks.length;i++){totalDataCount+=rsBlocks[i].dataCount}for(var i=0;i<this.dataList.length;i++){var data=this.dataList[i];buffer.put(data.mode,4);buffer.put(data.getLength(),QRUtil.getLengthInBits(data.mode,typeNumber));data.write(buffer)}if(buffer.getLengthInBits()<=totalDataCount*8){break}}this.typeNumber=typeNumber}this.makeImpl(false,this.getBestMaskPattern())},makeImpl:function(test,maskPattern){this.moduleCount=this.typeNumber*4+17;this.modules=new Array(this.moduleCount);for(var row=0;row<this.moduleCount;row++){this.modules[row]=new Array(this.moduleCount);for(var col=0;col<this.moduleCount;col++){this.modules[row][col]=null}}this.setupPositionProbePattern(0,0);this.setupPositionProbePattern(this.moduleCount-7,0);this.setupPositionProbePattern(0,this.moduleCount-7);this.setupPositionAdjustPattern();this.setupTimingPattern();this.setupTypeInfo(test,maskPattern);if(this.typeNumber>=7){this.setupTypeNumber(test)}if(this.dataCache==null){this.dataCache=QRCode.createData(this.typeNumber,this.errorCorrectLevel,this.dataList)}this.mapData(this.dataCache,maskPattern)},setupPositionProbePattern:function(row,col){for(var r=-1;r<=7;r++){if(row+r<=-1||this.moduleCount<=row+r){continue}for(var c=-1;c<=7;c++){if(col+c<=-1||this.moduleCount<=col+c){continue}if((0<=r&&r<=6&&(c==0||c==6))||(0<=c&&c<=6&&(r==0||r==6))||(2<=r&&r<=4&&2<=c&&c<=4)){this.modules[row+r][col+c]=true}else{this.modules[row+r][col+c]=false}}}},getBestMaskPattern:function(){var minLostPoint=0;var pattern=0;for(var i=0;i<8;i++){this.makeImpl(true,i);var lostPoint=QRUtil.getLostPoint(this);if(i==0||minLostPoint>lostPoint){minLostPoint=lostPoint;pattern=i}}return pattern},createMovieClip:function(target_mc,instance_name,depth){var qr_mc=target_mc.createEmptyMovieClip(instance_name,depth);var cs=1;this.make();for(var row=0;row<this.modules.length;row++){var y=row*cs;for(var col=0;col<this.modules[row].length;col++){var x=col*cs;var dark=this.modules[row][col];if(dark){qr_mc.beginFill(0,100);qr_mc.moveTo(x,y);qr_mc.lineTo(x+cs,y);qr_mc.lineTo(x+cs,y+cs);qr_mc.lineTo(x,y+cs);qr_mc.endFill()}}}return qr_mc},setupTimingPattern:function(){for(var r=8;r<this.moduleCount-8;r++){if(this.modules[r][6]!=null){continue}this.modules[r][6]=(r%2==0)}for(var c=8;c<this.moduleCount-8;c++){if(this.modules[6][c]!=null){continue}this.modules[6][c]=(c%2==0)}},setupPositionAdjustPattern:function(){var pos=QRUtil.getPatternPosition(this.typeNumber);for(var i=0;i<pos.length;i++){for(var j=0;j<pos.length;j++){var row=pos[i];var col=pos[j];if(this.modules[row][col]!=null){continue}for(var r=-2;r<=2;r++){for(var c=-2;c<=2;c++){if(r==-2||r==2||c==-2||c==2||(r==0&&c==0)){this.modules[row+r][col+c]=true}else{this.modules[row+r][col+c]=false}}}}}},setupTypeNumber:function(test){var bits=QRUtil.getBCHTypeNumber(this.typeNumber);for(var i=0;i<18;i++){var mod=(!test&&((bits>>i)&1)==1);this.modules[Math.floor(i/3)][i%3+this.moduleCount-8-3]=mod}for(var i=0;i<18;i++){var mod=(!test&&((bits>>i)&1)==1);this.modules[i%3+this.moduleCount-8-3][Math.floor(i/3)]=mod}},setupTypeInfo:function(test,maskPattern){var data=(this.errorCorrectLevel<<3)|maskPattern;var bits=QRUtil.getBCHTypeInfo(data);for(var i=0;i<15;i++){var mod=(!test&&((bits>>i)&1)==1);if(i<6){this.modules[i][8]=mod}else{if(i<8){this.modules[i+1][8]=mod}else{this.modules[this.moduleCount-15+i][8]=mod}}}for(var i=0;i<15;i++){var mod=(!test&&((bits>>i)&1)==1);if(i<8){this.modules[8][this.moduleCount-i-1]=mod}else{if(i<9){this.modules[8][15-i-1+1]=mod}else{this.modules[8][15-i-1]=mod}}}this.modules[this.moduleCount-8][8]=(!test)},mapData:function(data,maskPattern){var inc=-1;var row=this.moduleCount-1;var bitIndex=7;var byteIndex=0;for(var col=this.moduleCount-1;col>0;col-=2){if(col==6){col--}while(true){for(var c=0;c<2;c++){if(this.modules[row][col-c]==null){var dark=false;if(byteIndex<data.length){dark=(((data[byteIndex]>>>bitIndex)&1)==1)}var mask=QRUtil.getMask(maskPattern,row,col-c);if(mask){dark=!dark}this.modules[row][col-c]=dark;bitIndex--;if(bitIndex==-1){byteIndex++;
bitIndex=7}}}row+=inc;if(row<0||this.moduleCount<=row){row-=inc;inc=-inc;break}}}}};QRCode.PAD0=236;QRCode.PAD1=17;QRCode.createData=function(typeNumber,errorCorrectLevel,dataList){var rsBlocks=QRRSBlock.getRSBlocks(typeNumber,errorCorrectLevel);var buffer=new QRBitBuffer();for(var i=0;i<dataList.length;i++){var data=dataList[i];buffer.put(data.mode,4);buffer.put(data.getLength(),QRUtil.getLengthInBits(data.mode,typeNumber));data.write(buffer)}var totalDataCount=0;for(var i=0;i<rsBlocks.length;i++){totalDataCount+=rsBlocks[i].dataCount}if(buffer.getLengthInBits()>totalDataCount*8){throw new Error("code length overflow. ("+buffer.getLengthInBits()+">"+totalDataCount*8+")")}if(buffer.getLengthInBits()+4<=totalDataCount*8){buffer.put(0,4)}while(buffer.getLengthInBits()%8!=0){buffer.putBit(false)}while(true){if(buffer.getLengthInBits()>=totalDataCount*8){break}buffer.put(QRCode.PAD0,8);if(buffer.getLengthInBits()>=totalDataCount*8){break}buffer.put(QRCode.PAD1,8)}return QRCode.createBytes(buffer,rsBlocks)};QRCode.createBytes=function(buffer,rsBlocks){var offset=0;var maxDcCount=0;var maxEcCount=0;var dcdata=new Array(rsBlocks.length);var ecdata=new Array(rsBlocks.length);for(var r=0;r<rsBlocks.length;r++){var dcCount=rsBlocks[r].dataCount;var ecCount=rsBlocks[r].totalCount-dcCount;maxDcCount=Math.max(maxDcCount,dcCount);maxEcCount=Math.max(maxEcCount,ecCount);dcdata[r]=new Array(dcCount);for(var i=0;i<dcdata[r].length;i++){dcdata[r][i]=255&buffer.buffer[i+offset]}offset+=dcCount;var rsPoly=QRUtil.getErrorCorrectPolynomial(ecCount);var rawPoly=new QRPolynomial(dcdata[r],rsPoly.getLength()-1);var modPoly=rawPoly.mod(rsPoly);ecdata[r]=new Array(rsPoly.getLength()-1);for(var i=0;i<ecdata[r].length;i++){var modIndex=i+modPoly.getLength()-ecdata[r].length;ecdata[r][i]=(modIndex>=0)?modPoly.get(modIndex):0}}var totalCodeCount=0;for(var i=0;i<rsBlocks.length;i++){totalCodeCount+=rsBlocks[i].totalCount}var data=new Array(totalCodeCount);var index=0;for(var i=0;i<maxDcCount;i++){for(var r=0;r<rsBlocks.length;r++){if(i<dcdata[r].length){data[index++]=dcdata[r][i]}}}for(var i=0;i<maxEcCount;i++){for(var r=0;r<rsBlocks.length;r++){if(i<ecdata[r].length){data[index++]=ecdata[r][i]}}}return data};var QRMode={MODE_NUMBER:1<<0,MODE_ALPHA_NUM:1<<1,MODE_8BIT_BYTE:1<<2,MODE_KANJI:1<<3};var QRErrorCorrectLevel={L:1,M:0,Q:3,H:2};var QRMaskPattern={PATTERN000:0,PATTERN001:1,PATTERN010:2,PATTERN011:3,PATTERN100:4,PATTERN101:5,PATTERN110:6,PATTERN111:7};var QRUtil={PATTERN_POSITION_TABLE:[[],[6,18],[6,22],[6,26],[6,30],[6,34],[6,22,38],[6,24,42],[6,26,46],[6,28,50],[6,30,54],[6,32,58],[6,34,62],[6,26,46,66],[6,26,48,70],[6,26,50,74],[6,30,54,78],[6,30,56,82],[6,30,58,86],[6,34,62,90],[6,28,50,72,94],[6,26,50,74,98],[6,30,54,78,102],[6,28,54,80,106],[6,32,58,84,110],[6,30,58,86,114],[6,34,62,90,118],[6,26,50,74,98,122],[6,30,54,78,102,126],[6,26,52,78,104,130],[6,30,56,82,108,134],[6,34,60,86,112,138],[6,30,58,86,114,142],[6,34,62,90,118,146],[6,30,54,78,102,126,150],[6,24,50,76,102,128,154],[6,28,54,80,106,132,158],[6,32,58,84,110,136,162],[6,26,54,82,110,138,166],[6,30,58,86,114,142,170]],G15:(1<<10)|(1<<8)|(1<<5)|(1<<4)|(1<<2)|(1<<1)|(1<<0),G18:(1<<12)|(1<<11)|(1<<10)|(1<<9)|(1<<8)|(1<<5)|(1<<2)|(1<<0),G15_MASK:(1<<14)|(1<<12)|(1<<10)|(1<<4)|(1<<1),getBCHTypeInfo:function(data){var d=data<<10;while(QRUtil.getBCHDigit(d)-QRUtil.getBCHDigit(QRUtil.G15)>=0){d^=(QRUtil.G15<<(QRUtil.getBCHDigit(d)-QRUtil.getBCHDigit(QRUtil.G15)))}return((data<<10)|d)^QRUtil.G15_MASK},getBCHTypeNumber:function(data){var d=data<<12;while(QRUtil.getBCHDigit(d)-QRUtil.getBCHDigit(QRUtil.G18)>=0){d^=(QRUtil.G18<<(QRUtil.getBCHDigit(d)-QRUtil.getBCHDigit(QRUtil.G18)))}return(data<<12)|d},getBCHDigit:function(data){var digit=0;while(data!=0){digit++;data>>>=1}return digit},getPatternPosition:function(typeNumber){return QRUtil.PATTERN_POSITION_TABLE[typeNumber-1]},getMask:function(maskPattern,i,j){switch(maskPattern){case QRMaskPattern.PATTERN000:return(i+j)%2==0;case QRMaskPattern.PATTERN001:return i%2==0;case QRMaskPattern.PATTERN010:return j%3==0;case QRMaskPattern.PATTERN011:return(i+j)%3==0;case QRMaskPattern.PATTERN100:return(Math.floor(i/2)+Math.floor(j/3))%2==0;case QRMaskPattern.PATTERN101:return(i*j)%2+(i*j)%3==0;case QRMaskPattern.PATTERN110:return((i*j)%2+(i*j)%3)%2==0;case QRMaskPattern.PATTERN111:return((i*j)%3+(i+j)%2)%2==0;default:throw new Error("bad maskPattern:"+maskPattern)}},getErrorCorrectPolynomial:function(errorCorrectLength){var a=new QRPolynomial([1],0);for(var i=0;i<errorCorrectLength;i++){a=a.multiply(new QRPolynomial([1,QRMath.gexp(i)],0))}return a},getLengthInBits:function(mode,type){if(1<=type&&type<10){switch(mode){case QRMode.MODE_NUMBER:return 10;case QRMode.MODE_ALPHA_NUM:return 9;case QRMode.MODE_8BIT_BYTE:return 8;case QRMode.MODE_KANJI:return 8;default:throw new Error("mode:"+mode)}}else{if(type<27){switch(mode){case QRMode.MODE_NUMBER:return 12;case QRMode.MODE_ALPHA_NUM:return 11;case QRMode.MODE_8BIT_BYTE:return 16;case QRMode.MODE_KANJI:return 10;
default:throw new Error("mode:"+mode)}}else{if(type<41){switch(mode){case QRMode.MODE_NUMBER:return 14;case QRMode.MODE_ALPHA_NUM:return 13;case QRMode.MODE_8BIT_BYTE:return 16;case QRMode.MODE_KANJI:return 12;default:throw new Error("mode:"+mode)}}else{throw new Error("type:"+type)}}}},getLostPoint:function(qrCode){var moduleCount=qrCode.getModuleCount();var lostPoint=0;for(var row=0;row<moduleCount;row++){for(var col=0;col<moduleCount;col++){var sameCount=0;var dark=qrCode.isDark(row,col);for(var r=-1;r<=1;r++){if(row+r<0||moduleCount<=row+r){continue}for(var c=-1;c<=1;c++){if(col+c<0||moduleCount<=col+c){continue}if(r==0&&c==0){continue}if(dark==qrCode.isDark(row+r,col+c)){sameCount++}}}if(sameCount>5){lostPoint+=(3+sameCount-5)}}}for(var row=0;row<moduleCount-1;row++){for(var col=0;col<moduleCount-1;col++){var count=0;if(qrCode.isDark(row,col)){count++}if(qrCode.isDark(row+1,col)){count++}if(qrCode.isDark(row,col+1)){count++}if(qrCode.isDark(row+1,col+1)){count++}if(count==0||count==4){lostPoint+=3}}}for(var row=0;row<moduleCount;row++){for(var col=0;col<moduleCount-6;col++){if(qrCode.isDark(row,col)&&!qrCode.isDark(row,col+1)&&qrCode.isDark(row,col+2)&&qrCode.isDark(row,col+3)&&qrCode.isDark(row,col+4)&&!qrCode.isDark(row,col+5)&&qrCode.isDark(row,col+6)){lostPoint+=40}}}for(var col=0;col<moduleCount;col++){for(var row=0;row<moduleCount-6;row++){if(qrCode.isDark(row,col)&&!qrCode.isDark(row+1,col)&&qrCode.isDark(row+2,col)&&qrCode.isDark(row+3,col)&&qrCode.isDark(row+4,col)&&!qrCode.isDark(row+5,col)&&qrCode.isDark(row+6,col)){lostPoint+=40}}}var darkCount=0;for(var col=0;col<moduleCount;col++){for(var row=0;row<moduleCount;row++){if(qrCode.isDark(row,col)){darkCount++}}}var ratio=Math.abs(100*darkCount/moduleCount/moduleCount-50)/5;lostPoint+=ratio*10;return lostPoint}};var QRMath={glog:function(n){if(n<1){throw new Error("glog("+n+")")}return QRMath.LOG_TABLE[n]},gexp:function(n){while(n<0){n+=255}while(n>=256){n-=255}return QRMath.EXP_TABLE[n]},EXP_TABLE:new Array(256),LOG_TABLE:new Array(256)};for(var i=0;i<8;i++){QRMath.EXP_TABLE[i]=1<<i}for(var i=8;i<256;i++){QRMath.EXP_TABLE[i]=QRMath.EXP_TABLE[i-4]^QRMath.EXP_TABLE[i-5]^QRMath.EXP_TABLE[i-6]^QRMath.EXP_TABLE[i-8]}for(var i=0;i<255;i++){QRMath.LOG_TABLE[QRMath.EXP_TABLE[i]]=i}function QRPolynomial(num,shift){if(num.length==undefined){throw new Error(num.length+"/"+shift)}var offset=0;while(offset<num.length&&num[offset]==0){offset++}this.num=new Array(num.length-offset+shift);for(var i=0;i<num.length-offset;i++){this.num[i]=num[i+offset]}}QRPolynomial.prototype={get:function(index){return this.num[index]},getLength:function(){return this.num.length},multiply:function(e){var num=new Array(this.getLength()+e.getLength()-1);for(var i=0;i<this.getLength();i++){for(var j=0;j<e.getLength();j++){num[i+j]^=QRMath.gexp(QRMath.glog(this.get(i))+QRMath.glog(e.get(j)))}}return new QRPolynomial(num,0)},mod:function(e){if(this.getLength()-e.getLength()<0){return this}var ratio=QRMath.glog(this.get(0))-QRMath.glog(e.get(0));var num=new Array(this.getLength());for(var i=0;i<this.getLength();i++){num[i]=this.get(i)}for(var i=0;i<e.getLength();i++){num[i]^=QRMath.gexp(QRMath.glog(e.get(i))+ratio)}return new QRPolynomial(num,0).mod(e)}};function QRRSBlock(totalCount,dataCount){this.totalCount=totalCount;this.dataCount=dataCount}QRRSBlock.RS_BLOCK_TABLE=[[1,26,19],[1,26,16],[1,26,13],[1,26,9],[1,44,34],[1,44,28],[1,44,22],[1,44,16],[1,70,55],[1,70,44],[2,35,17],[2,35,13],[1,100,80],[2,50,32],[2,50,24],[4,25,9],[1,134,108],[2,67,43],[2,33,15,2,34,16],[2,33,11,2,34,12],[2,86,68],[4,43,27],[4,43,19],[4,43,15],[2,98,78],[4,49,31],[2,32,14,4,33,15],[4,39,13,1,40,14],[2,121,97],[2,60,38,2,61,39],[4,40,18,2,41,19],[4,40,14,2,41,15],[2,146,116],[3,58,36,2,59,37],[4,36,16,4,37,17],[4,36,12,4,37,13],[2,86,68,2,87,69],[4,69,43,1,70,44],[6,43,19,2,44,20],[6,43,15,2,44,16],[4,101,81],[1,80,50,4,81,51],[4,50,22,4,51,23],[3,36,12,8,37,13],[2,116,92,2,117,93],[6,58,36,2,59,37],[4,46,20,6,47,21],[7,42,14,4,43,15],[4,133,107],[8,59,37,1,60,38],[8,44,20,4,45,21],[12,33,11,4,34,12],[3,145,115,1,146,116],[4,64,40,5,65,41],[11,36,16,5,37,17],[11,36,12,5,37,13],[5,109,87,1,110,88],[5,65,41,5,66,42],[5,54,24,7,55,25],[11,36,12],[5,122,98,1,123,99],[7,73,45,3,74,46],[15,43,19,2,44,20],[3,45,15,13,46,16],[1,135,107,5,136,108],[10,74,46,1,75,47],[1,50,22,15,51,23],[2,42,14,17,43,15],[5,150,120,1,151,121],[9,69,43,4,70,44],[17,50,22,1,51,23],[2,42,14,19,43,15],[3,141,113,4,142,114],[3,70,44,11,71,45],[17,47,21,4,48,22],[9,39,13,16,40,14],[3,135,107,5,136,108],[3,67,41,13,68,42],[15,54,24,5,55,25],[15,43,15,10,44,16],[4,144,116,4,145,117],[17,68,42],[17,50,22,6,51,23],[19,46,16,6,47,17],[2,139,111,7,140,112],[17,74,46],[7,54,24,16,55,25],[34,37,13],[4,151,121,5,152,122],[4,75,47,14,76,48],[11,54,24,14,55,25],[16,45,15,14,46,16],[6,147,117,4,148,118],[6,73,45,14,74,46],[11,54,24,16,55,25],[30,46,16,2,47,17],[8,132,106,4,133,107],[8,75,47,13,76,48],[7,54,24,22,55,25],[22,45,15,13,46,16],[10,142,114,2,143,115],[19,74,46,4,75,47],[28,50,22,6,51,23],[33,46,16,4,47,17],[8,152,122,4,153,123],[22,73,45,3,74,46],[8,53,23,26,54,24],[12,45,15,28,46,16],[3,147,117,10,148,118],[3,73,45,23,74,46],[4,54,24,31,55,25],[11,45,15,31,46,16],[7,146,116,7,147,117],[21,73,45,7,74,46],[1,53,23,37,54,24],[19,45,15,26,46,16],[5,145,115,10,146,116],[19,75,47,10,76,48],[15,54,24,25,55,25],[23,45,15,25,46,16],[13,145,115,3,146,116],[2,74,46,29,75,47],[42,54,24,1,55,25],[23,45,15,28,46,16],[17,145,115],[10,74,46,23,75,47],[10,54,24,35,55,25],[19,45,15,35,46,16],[17,145,115,1,146,116],[14,74,46,21,75,47],[29,54,24,19,55,25],[11,45,15,46,46,16],[13,145,115,6,146,116],[14,74,46,23,75,47],[44,54,24,7,55,25],[59,46,16,1,47,17],[12,151,121,7,152,122],[12,75,47,26,76,48],[39,54,24,14,55,25],[22,45,15,41,46,16],[6,151,121,14,152,122],[6,75,47,34,76,48],[46,54,24,10,55,25],[2,45,15,64,46,16],[17,152,122,4,153,123],[29,74,46,14,75,47],[49,54,24,10,55,25],[24,45,15,46,46,16],[4,152,122,18,153,123],[13,74,46,32,75,47],[48,54,24,14,55,25],[42,45,15,32,46,16],[20,147,117,4,148,118],[40,75,47,7,76,48],[43,54,24,22,55,25],[10,45,15,67,46,16],[19,148,118,6,149,119],[18,75,47,31,76,48],[34,54,24,34,55,25],[20,45,15,61,46,16]];
QRRSBlock.getRSBlocks=function(typeNumber,errorCorrectLevel){var rsBlock=QRRSBlock.getRsBlockTable(typeNumber,errorCorrectLevel);if(rsBlock==undefined){throw new Error("bad rs block @ typeNumber:"+typeNumber+"/errorCorrectLevel:"+errorCorrectLevel)}var length=rsBlock.length/3;var list=new Array();for(var i=0;i<length;i++){var count=rsBlock[i*3+0];var totalCount=rsBlock[i*3+1];var dataCount=rsBlock[i*3+2];for(var j=0;j<count;j++){list.push(new QRRSBlock(totalCount,dataCount))}}return list};QRRSBlock.getRsBlockTable=function(typeNumber,errorCorrectLevel){switch(errorCorrectLevel){case QRErrorCorrectLevel.L:return QRRSBlock.RS_BLOCK_TABLE[(typeNumber-1)*4+0];case QRErrorCorrectLevel.M:return QRRSBlock.RS_BLOCK_TABLE[(typeNumber-1)*4+1];case QRErrorCorrectLevel.Q:return QRRSBlock.RS_BLOCK_TABLE[(typeNumber-1)*4+2];case QRErrorCorrectLevel.H:return QRRSBlock.RS_BLOCK_TABLE[(typeNumber-1)*4+3];default:return undefined}};function QRBitBuffer(){this.buffer=new Array();this.length=0}QRBitBuffer.prototype={get:function(index){var bufIndex=Math.floor(index/8);return((this.buffer[bufIndex]>>>(7-index%8))&1)==1},put:function(num,length){for(var i=0;i<length;i++){this.putBit(((num>>>(length-i-1))&1)==1)}},getLengthInBits:function(){return this.length},putBit:function(bit){var bufIndex=Math.floor(this.length/8);if(this.buffer.length<=bufIndex){this.buffer.push(0)}if(bit){this.buffer[bufIndex]|=(128>>>(this.length%8))}this.length++}};

(function($){$.fn.qrcode=function(options){if(typeof options==="string"){options={text:options}}options=$.extend({},{render:"canvas",width:256,height:256,typeNumber:-1,correctLevel:QRErrorCorrectLevel.H,background:"#ffffff",foreground:"#000000"},options);var createCanvas=function(){var qrcode=new QRCode(options.typeNumber,options.correctLevel);qrcode.addData(options.text);qrcode.make();var canvas=document.createElement("canvas");if(!canvas.getContext){return}canvas.width=options.width;canvas.height=options.height;var ctx=canvas.getContext("2d");var tileW=options.width/qrcode.getModuleCount();var tileH=options.height/qrcode.getModuleCount();for(var row=0;row<qrcode.getModuleCount();row++){for(var col=0;col<qrcode.getModuleCount();col++){ctx.fillStyle=qrcode.isDark(row,col)?options.foreground:options.background;var w=(Math.ceil((col+1)*tileW)-Math.floor(col*tileW));var h=(Math.ceil((row+1)*tileW)-Math.floor(row*tileW));ctx.fillRect(Math.round(col*tileW),Math.round(row*tileH),w,h)}}return canvas};var createTable=function(){var qrcode=new QRCode(options.typeNumber,options.correctLevel);qrcode.addData(options.text);qrcode.make();var $table=$("<table></table>").css("width",options.width+"px").css("height",options.height+"px").css("border","0px").css("border-collapse","collapse").css("background-color",options.background);var tileW=options.width/qrcode.getModuleCount();var tileH=options.height/qrcode.getModuleCount();for(var row=0;row<qrcode.getModuleCount();row++){var $row=$("<tr></tr>").css("height",tileH+"px").appendTo($table);for(var col=0;col<qrcode.getModuleCount();col++){$("<td></td>").css("width",tileW+"px").css("background-color",qrcode.isDark(row,col)?options.foreground:options.background).appendTo($row)}}return $table};return this.each(function(){var element=options.render=="canvas"?createCanvas():createTable();$(element).appendTo(this)})}})(jQuery);

/*fileOverview TouchSwipe - jQuery Plugin version 1.6.6 * author Matt Bryson http://www.github.com/mattbryson *Copyright (c) 2010-2015 Matt Bryson Dual licensed under the MIT or GPL Version 2 licenses.*/
(function(factory){if(typeof define==="function"&&define.amd&&define.amd.jQuery){define(["jquery"],factory)}else{factory(jQuery)}}(function($){var LEFT="left",RIGHT="right",UP="up",DOWN="down",IN="in",OUT="out",NONE="none",AUTO="auto",SWIPE="swipe",PINCH="pinch",TAP="tap",DOUBLE_TAP="doubletap",LONG_TAP="longtap",HOLD="hold",HORIZONTAL="horizontal",VERTICAL="vertical",ALL_FINGERS="all",DOUBLE_TAP_THRESHOLD=10,PHASE_START="start",PHASE_MOVE="move",PHASE_END="end",PHASE_CANCEL="cancel",SUPPORTS_TOUCH="ontouchstart" in window,SUPPORTS_POINTER_IE10=window.navigator.msPointerEnabled&&!window.navigator.pointerEnabled,SUPPORTS_POINTER=window.navigator.pointerEnabled||window.navigator.msPointerEnabled,PLUGIN_NS="TouchSwipe";var defaults={fingers:1,threshold:75,cancelThreshold:null,pinchThreshold:20,maxTimeThreshold:null,fingerReleaseThreshold:250,longTapThreshold:500,doubleTapThreshold:200,swipe:null,swipeLeft:null,swipeRight:null,swipeUp:null,swipeDown:null,swipeStatus:null,pinchIn:null,pinchOut:null,pinchStatus:null,click:null,tap:null,doubleTap:null,longTap:null,hold:null,triggerOnTouchEnd:true,triggerOnTouchLeave:false,allowPageScroll:"auto",fallbackToMouseEvents:true,excludedElements:"label, button, input, select, textarea, a, .noSwipe",preventDefaultEvents:true};$.fn.swipe=function(method){var $this=$(this),plugin=$this.data(PLUGIN_NS);if(plugin&&typeof method==="string"){if(plugin[method]){return plugin[method].apply(this,Array.prototype.slice.call(arguments,1))}else{$.error("Method "+method+" does not exist on jQuery.swipe")}}else{if(!plugin&&(typeof method==="object"||!method)){return init.apply(this,arguments)}}return $this};$.fn.swipe.defaults=defaults;$.fn.swipe.phases={PHASE_START:PHASE_START,PHASE_MOVE:PHASE_MOVE,PHASE_END:PHASE_END,PHASE_CANCEL:PHASE_CANCEL};$.fn.swipe.directions={LEFT:LEFT,RIGHT:RIGHT,UP:UP,DOWN:DOWN,IN:IN,OUT:OUT};$.fn.swipe.pageScroll={NONE:NONE,HORIZONTAL:HORIZONTAL,VERTICAL:VERTICAL,AUTO:AUTO};$.fn.swipe.fingers={ONE:1,TWO:2,THREE:3,ALL:ALL_FINGERS};function init(options){if(options&&(options.allowPageScroll===undefined&&(options.swipe!==undefined||options.swipeStatus!==undefined))){options.allowPageScroll=NONE}if(options.click!==undefined&&options.tap===undefined){options.tap=options.click}if(!options){options={}}options=$.extend({},$.fn.swipe.defaults,options);return this.each(function(){var $this=$(this);var plugin=$this.data(PLUGIN_NS);if(!plugin){plugin=new TouchSwipe(this,options);$this.data(PLUGIN_NS,plugin)}})}function TouchSwipe(element,options){var useTouchEvents=(SUPPORTS_TOUCH||SUPPORTS_POINTER||!options.fallbackToMouseEvents),START_EV=useTouchEvents?(SUPPORTS_POINTER?(SUPPORTS_POINTER_IE10?"MSPointerDown":"pointerdown"):"touchstart"):"mousedown",MOVE_EV=useTouchEvents?(SUPPORTS_POINTER?(SUPPORTS_POINTER_IE10?"MSPointerMove":"pointermove"):"touchmove"):"mousemove",END_EV=useTouchEvents?(SUPPORTS_POINTER?(SUPPORTS_POINTER_IE10?"MSPointerUp":"pointerup"):"touchend"):"mouseup",LEAVE_EV=useTouchEvents?null:"mouseleave",CANCEL_EV=(SUPPORTS_POINTER?(SUPPORTS_POINTER_IE10?"MSPointerCancel":"pointercancel"):"touchcancel");var distance=0,direction=null,duration=0,startTouchesDistance=0,endTouchesDistance=0,pinchZoom=1,pinchDistance=0,pinchDirection=0,maximumsMap=null;var $element=$(element);var phase="start";var fingerCount=0;var fingerData=null;var startTime=0,endTime=0,previousTouchEndTime=0,previousTouchFingerCount=0,doubleTapStartTime=0;var singleTapTimeout=null,holdTimeout=null;try{$element.bind(START_EV,touchStart);$element.bind(CANCEL_EV,touchCancel)}catch(e){$.error("events not supported "+START_EV+","+CANCEL_EV+" on jQuery.swipe")}this.enable=function(){$element.bind(START_EV,touchStart);$element.bind(CANCEL_EV,touchCancel);return $element};this.disable=function(){removeListeners();return $element};this.destroy=function(){removeListeners();$element.data(PLUGIN_NS,null);$element=null};this.option=function(property,value){if(options[property]!==undefined){if(value===undefined){return options[property]}else{options[property]=value}}else{$.error("Option "+property+" does not exist on jQuery.swipe.options")}return null};function touchStart(jqEvent){if(getTouchInProgress()){return}if($(jqEvent.target).closest(options.excludedElements,$element).length>0){return}var event=jqEvent.originalEvent?jqEvent.originalEvent:jqEvent;var ret,evt=SUPPORTS_TOUCH?event.touches[0]:event;phase=PHASE_START;if(SUPPORTS_TOUCH){fingerCount=event.touches.length}else{jqEvent.preventDefault()}distance=0;direction=null;pinchDirection=null;duration=0;startTouchesDistance=0;endTouchesDistance=0;pinchZoom=1;pinchDistance=0;fingerData=createAllFingerData();maximumsMap=createMaximumsData();cancelMultiFingerRelease();if(!SUPPORTS_TOUCH||(fingerCount===options.fingers||options.fingers===ALL_FINGERS)||hasPinches()){createFingerData(0,evt);startTime=getTimeStamp();if(fingerCount==2){createFingerData(1,event.touches[1]);startTouchesDistance=endTouchesDistance=calculateTouchesDistance(fingerData[0].start,fingerData[1].start)
}if(options.swipeStatus||options.pinchStatus){ret=triggerHandler(event,phase)}}else{ret=false}if(ret===false){phase=PHASE_CANCEL;triggerHandler(event,phase);return ret}else{if(options.hold){holdTimeout=setTimeout($.proxy(function(){$element.trigger("hold",[event.target]);if(options.hold){ret=options.hold.call($element,event,event.target)}},this),options.longTapThreshold)}setTouchInProgress(true)}return null}function touchMove(jqEvent){var event=jqEvent.originalEvent?jqEvent.originalEvent:jqEvent;if(phase===PHASE_END||phase===PHASE_CANCEL||inMultiFingerRelease()){return}var ret,evt=SUPPORTS_TOUCH?event.touches[0]:event;var currentFinger=updateFingerData(evt);endTime=getTimeStamp();if(SUPPORTS_TOUCH){fingerCount=event.touches.length}if(options.hold){clearTimeout(holdTimeout)}phase=PHASE_MOVE;if(fingerCount==2){if(startTouchesDistance==0){createFingerData(1,event.touches[1]);startTouchesDistance=endTouchesDistance=calculateTouchesDistance(fingerData[0].start,fingerData[1].start)}else{updateFingerData(event.touches[1]);endTouchesDistance=calculateTouchesDistance(fingerData[0].end,fingerData[1].end);pinchDirection=calculatePinchDirection(fingerData[0].end,fingerData[1].end)}pinchZoom=calculatePinchZoom(startTouchesDistance,endTouchesDistance);pinchDistance=Math.abs(startTouchesDistance-endTouchesDistance)}if((fingerCount===options.fingers||options.fingers===ALL_FINGERS)||!SUPPORTS_TOUCH||hasPinches()){direction=calculateDirection(currentFinger.start,currentFinger.end);validateDefaultEvent(jqEvent,direction);distance=calculateDistance(currentFinger.start,currentFinger.end);duration=calculateDuration();setMaxDistance(direction,distance);if(options.swipeStatus||options.pinchStatus){ret=triggerHandler(event,phase)}if(!options.triggerOnTouchEnd||options.triggerOnTouchLeave){var inBounds=true;if(options.triggerOnTouchLeave){var bounds=getbounds(this);inBounds=isInBounds(currentFinger.end,bounds)}if(!options.triggerOnTouchEnd&&inBounds){phase=getNextPhase(PHASE_MOVE)}else{if(options.triggerOnTouchLeave&&!inBounds){phase=getNextPhase(PHASE_END)}}if(phase==PHASE_CANCEL||phase==PHASE_END){triggerHandler(event,phase)}}}else{phase=PHASE_CANCEL;triggerHandler(event,phase)}if(ret===false){phase=PHASE_CANCEL;triggerHandler(event,phase)}}function touchEnd(jqEvent){var event=jqEvent.originalEvent;if(SUPPORTS_TOUCH){if(event.touches.length>0){startMultiFingerRelease();return true}}if(inMultiFingerRelease()){fingerCount=previousTouchFingerCount}endTime=getTimeStamp();duration=calculateDuration();if(didSwipeBackToCancel()||!validateSwipeDistance()){phase=PHASE_CANCEL;triggerHandler(event,phase)}else{if(options.triggerOnTouchEnd||(options.triggerOnTouchEnd==false&&phase===PHASE_MOVE)){jqEvent.preventDefault();phase=PHASE_END;triggerHandler(event,phase)}else{if(!options.triggerOnTouchEnd&&hasTap()){phase=PHASE_END;triggerHandlerForGesture(event,phase,TAP)}else{if(phase===PHASE_MOVE){phase=PHASE_CANCEL;triggerHandler(event,phase)}}}}setTouchInProgress(false);return null}function touchCancel(){fingerCount=0;endTime=0;startTime=0;startTouchesDistance=0;endTouchesDistance=0;pinchZoom=1;cancelMultiFingerRelease();setTouchInProgress(false)}function touchLeave(jqEvent){var event=jqEvent.originalEvent;if(options.triggerOnTouchLeave){phase=getNextPhase(PHASE_END);triggerHandler(event,phase)}}function removeListeners(){$element.unbind(START_EV,touchStart);$element.unbind(CANCEL_EV,touchCancel);$element.unbind(MOVE_EV,touchMove);$element.unbind(END_EV,touchEnd);if(LEAVE_EV){$element.unbind(LEAVE_EV,touchLeave)}setTouchInProgress(false)}function getNextPhase(currentPhase){var nextPhase=currentPhase;var validTime=validateSwipeTime();var validDistance=validateSwipeDistance();var didCancel=didSwipeBackToCancel();if(!validTime||didCancel){nextPhase=PHASE_CANCEL}else{if(validDistance&&currentPhase==PHASE_MOVE&&(!options.triggerOnTouchEnd||options.triggerOnTouchLeave)){nextPhase=PHASE_END}else{if(!validDistance&&currentPhase==PHASE_END&&options.triggerOnTouchLeave){nextPhase=PHASE_CANCEL}}}return nextPhase}function triggerHandler(event,phase){var ret=undefined;if((didSwipe()||hasSwipes())||(didPinch()||hasPinches())){if(didSwipe()||hasSwipes()){ret=triggerHandlerForGesture(event,phase,SWIPE)}if((didPinch()||hasPinches())&&ret!==false){ret=triggerHandlerForGesture(event,phase,PINCH)}}else{if(didDoubleTap()&&ret!==false){ret=triggerHandlerForGesture(event,phase,DOUBLE_TAP)}else{if(didLongTap()&&ret!==false){ret=triggerHandlerForGesture(event,phase,LONG_TAP)}else{if(didTap()&&ret!==false){ret=triggerHandlerForGesture(event,phase,TAP)}}}}if(phase===PHASE_CANCEL){touchCancel(event)}if(phase===PHASE_END){if(SUPPORTS_TOUCH){if(event.touches.length==0){touchCancel(event)}}else{touchCancel(event)}}return ret}function triggerHandlerForGesture(event,phase,gesture){var ret=undefined;if(gesture==SWIPE){$element.trigger("swipeStatus",[phase,direction||null,distance||0,duration||0,fingerCount,fingerData]);if(options.swipeStatus){ret=options.swipeStatus.call($element,event,phase,direction||null,distance||0,duration||0,fingerCount,fingerData);
if(ret===false){return false}}if(phase==PHASE_END&&validateSwipe()){$element.trigger("swipe",[direction,distance,duration,fingerCount,fingerData]);if(options.swipe){ret=options.swipe.call($element,event,direction,distance,duration,fingerCount,fingerData);if(ret===false){return false}}switch(direction){case LEFT:$element.trigger("swipeLeft",[direction,distance,duration,fingerCount,fingerData]);if(options.swipeLeft){ret=options.swipeLeft.call($element,event,direction,distance,duration,fingerCount,fingerData)}break;case RIGHT:$element.trigger("swipeRight",[direction,distance,duration,fingerCount,fingerData]);if(options.swipeRight){ret=options.swipeRight.call($element,event,direction,distance,duration,fingerCount,fingerData)}break;case UP:$element.trigger("swipeUp",[direction,distance,duration,fingerCount,fingerData]);if(options.swipeUp){ret=options.swipeUp.call($element,event,direction,distance,duration,fingerCount,fingerData)}break;case DOWN:$element.trigger("swipeDown",[direction,distance,duration,fingerCount,fingerData]);if(options.swipeDown){ret=options.swipeDown.call($element,event,direction,distance,duration,fingerCount,fingerData)}break}}}if(gesture==PINCH){$element.trigger("pinchStatus",[phase,pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData]);if(options.pinchStatus){ret=options.pinchStatus.call($element,event,phase,pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData);if(ret===false){return false}}if(phase==PHASE_END&&validatePinch()){switch(pinchDirection){case IN:$element.trigger("pinchIn",[pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData]);if(options.pinchIn){ret=options.pinchIn.call($element,event,pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData)}break;case OUT:$element.trigger("pinchOut",[pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData]);if(options.pinchOut){ret=options.pinchOut.call($element,event,pinchDirection||null,pinchDistance||0,duration||0,fingerCount,pinchZoom,fingerData)}break}}}if(gesture==TAP){if(phase===PHASE_CANCEL||phase===PHASE_END){clearTimeout(singleTapTimeout);clearTimeout(holdTimeout);if(hasDoubleTap()&&!inDoubleTap()){doubleTapStartTime=getTimeStamp();singleTapTimeout=setTimeout($.proxy(function(){doubleTapStartTime=null;$element.trigger("tap",[event.target]);if(options.tap){ret=options.tap.call($element,event,event.target)}},this),options.doubleTapThreshold)}else{doubleTapStartTime=null;$element.trigger("tap",[event.target]);if(options.tap){ret=options.tap.call($element,event,event.target)}}}}else{if(gesture==DOUBLE_TAP){if(phase===PHASE_CANCEL||phase===PHASE_END){clearTimeout(singleTapTimeout);doubleTapStartTime=null;$element.trigger("doubletap",[event.target]);if(options.doubleTap){ret=options.doubleTap.call($element,event,event.target)}}}else{if(gesture==LONG_TAP){if(phase===PHASE_CANCEL||phase===PHASE_END){clearTimeout(singleTapTimeout);doubleTapStartTime=null;$element.trigger("longtap",[event.target]);if(options.longTap){ret=options.longTap.call($element,event,event.target)}}}}}return ret}function validateSwipeDistance(){var valid=true;if(options.threshold!==null){valid=distance>=options.threshold}return valid}function didSwipeBackToCancel(){var cancelled=false;if(options.cancelThreshold!==null&&direction!==null){cancelled=(getMaxDistance(direction)-distance)>=options.cancelThreshold}return cancelled}function validatePinchDistance(){if(options.pinchThreshold!==null){return pinchDistance>=options.pinchThreshold}return true}function validateSwipeTime(){var result;if(options.maxTimeThreshold){if(duration>=options.maxTimeThreshold){result=false}else{result=true}}else{result=true}return result}function validateDefaultEvent(jqEvent,direction){if(options.preventDefaultEvents===false){return}if(options.allowPageScroll===NONE){jqEvent.preventDefault()}else{var auto=options.allowPageScroll===AUTO;switch(direction){case LEFT:if((options.swipeLeft&&auto)||(!auto&&options.allowPageScroll!=HORIZONTAL)){jqEvent.preventDefault()}break;case RIGHT:if((options.swipeRight&&auto)||(!auto&&options.allowPageScroll!=HORIZONTAL)){jqEvent.preventDefault()}break;case UP:if((options.swipeUp&&auto)||(!auto&&options.allowPageScroll!=VERTICAL)){jqEvent.preventDefault()}break;case DOWN:if((options.swipeDown&&auto)||(!auto&&options.allowPageScroll!=VERTICAL)){jqEvent.preventDefault()}break}}}function validatePinch(){var hasCorrectFingerCount=validateFingers();var hasEndPoint=validateEndPoint();var hasCorrectDistance=validatePinchDistance();return hasCorrectFingerCount&&hasEndPoint&&hasCorrectDistance}function hasPinches(){return !!(options.pinchStatus||options.pinchIn||options.pinchOut)}function didPinch(){return !!(validatePinch()&&hasPinches())}function validateSwipe(){var hasValidTime=validateSwipeTime();var hasValidDistance=validateSwipeDistance();var hasCorrectFingerCount=validateFingers();var hasEndPoint=validateEndPoint();var didCancel=didSwipeBackToCancel();
var valid=!didCancel&&hasEndPoint&&hasCorrectFingerCount&&hasValidDistance&&hasValidTime;return valid}function hasSwipes(){return !!(options.swipe||options.swipeStatus||options.swipeLeft||options.swipeRight||options.swipeUp||options.swipeDown)}function didSwipe(){return !!(validateSwipe()&&hasSwipes())}function validateFingers(){return((fingerCount===options.fingers||options.fingers===ALL_FINGERS)||!SUPPORTS_TOUCH)}function validateEndPoint(){return fingerData[0].end.x!==0}function hasTap(){return !!(options.tap)}function hasDoubleTap(){return !!(options.doubleTap)}function hasLongTap(){return !!(options.longTap)}function validateDoubleTap(){if(doubleTapStartTime==null){return false}var now=getTimeStamp();return(hasDoubleTap()&&((now-doubleTapStartTime)<=options.doubleTapThreshold))}function inDoubleTap(){return validateDoubleTap()}function validateTap(){return((fingerCount===1||!SUPPORTS_TOUCH)&&(isNaN(distance)||distance<options.threshold))}function validateLongTap(){return((duration>options.longTapThreshold)&&(distance<DOUBLE_TAP_THRESHOLD))}function didTap(){return !!(validateTap()&&hasTap())}function didDoubleTap(){return !!(validateDoubleTap()&&hasDoubleTap())}function didLongTap(){return !!(validateLongTap()&&hasLongTap())}function startMultiFingerRelease(){previousTouchEndTime=getTimeStamp();previousTouchFingerCount=event.touches.length+1}function cancelMultiFingerRelease(){previousTouchEndTime=0;previousTouchFingerCount=0}function inMultiFingerRelease(){var withinThreshold=false;if(previousTouchEndTime){var diff=getTimeStamp()-previousTouchEndTime;if(diff<=options.fingerReleaseThreshold){withinThreshold=true}}return withinThreshold}function getTouchInProgress(){return !!($element.data(PLUGIN_NS+"_intouch")===true)}function setTouchInProgress(val){if(val===true){$element.bind(MOVE_EV,touchMove);$element.bind(END_EV,touchEnd);if(LEAVE_EV){$element.bind(LEAVE_EV,touchLeave)}}else{$element.unbind(MOVE_EV,touchMove,false);$element.unbind(END_EV,touchEnd,false);if(LEAVE_EV){$element.unbind(LEAVE_EV,touchLeave,false)}}$element.data(PLUGIN_NS+"_intouch",val===true)}function createFingerData(index,evt){var id=evt.identifier!==undefined?evt.identifier:0;fingerData[index].identifier=id;fingerData[index].start.x=fingerData[index].end.x=evt.pageX||evt.clientX;fingerData[index].start.y=fingerData[index].end.y=evt.pageY||evt.clientY;return fingerData[index]}function updateFingerData(evt){var id=evt.identifier!==undefined?evt.identifier:0;var f=getFingerData(id);f.end.x=evt.pageX||evt.clientX;f.end.y=evt.pageY||evt.clientY;return f}function getFingerData(id){for(var i=0;i<fingerData.length;i++){if(fingerData[i].identifier==id){return fingerData[i]}}}function createAllFingerData(){var fingerData=[];for(var i=0;i<=5;i++){fingerData.push({start:{x:0,y:0},end:{x:0,y:0},identifier:0})}return fingerData}function setMaxDistance(direction,distance){distance=Math.max(distance,getMaxDistance(direction));maximumsMap[direction].distance=distance}function getMaxDistance(direction){if(maximumsMap[direction]){return maximumsMap[direction].distance}return undefined}function createMaximumsData(){var maxData={};maxData[LEFT]=createMaximumVO(LEFT);maxData[RIGHT]=createMaximumVO(RIGHT);maxData[UP]=createMaximumVO(UP);maxData[DOWN]=createMaximumVO(DOWN);return maxData}function createMaximumVO(dir){return{direction:dir,distance:0}}function calculateDuration(){return endTime-startTime}function calculateTouchesDistance(startPoint,endPoint){var diffX=Math.abs(startPoint.x-endPoint.x);var diffY=Math.abs(startPoint.y-endPoint.y);return Math.round(Math.sqrt(diffX*diffX+diffY*diffY))}function calculatePinchZoom(startDistance,endDistance){var percent=(endDistance/startDistance)*1;return percent.toFixed(2)}function calculatePinchDirection(){if(pinchZoom<1){return OUT}else{return IN}}function calculateDistance(startPoint,endPoint){return Math.round(Math.sqrt(Math.pow(endPoint.x-startPoint.x,2)+Math.pow(endPoint.y-startPoint.y,2)))}function calculateAngle(startPoint,endPoint){var x=startPoint.x-endPoint.x;var y=endPoint.y-startPoint.y;var r=Math.atan2(y,x);var angle=Math.round(r*180/Math.PI);if(angle<0){angle=360-Math.abs(angle)}return angle}function calculateDirection(startPoint,endPoint){var angle=calculateAngle(startPoint,endPoint);if((angle<=45)&&(angle>=0)){return LEFT}else{if((angle<=360)&&(angle>=315)){return LEFT}else{if((angle>=135)&&(angle<=225)){return RIGHT}else{if((angle>45)&&(angle<135)){return DOWN}else{return UP}}}}}function getTimeStamp(){var now=new Date();return now.getTime()}function getbounds(el){el=$(el);var offset=el.offset();var bounds={left:offset.left,right:offset.left+el.outerWidth(),top:offset.top,bottom:offset.top+el.outerHeight()};return bounds}function isInBounds(point,bounds){return(point.x>bounds.left&&point.x<bounds.right&&point.y>bounds.top&&point.y<bounds.bottom)}}}));

/*FastClick @codingstandard ftlabs-jsv2 * @copyright The Financial Times Limited [All Rights Reserved]	 * @license MIT License (see LICENSE.txt)*/
(function(){function FastClick(layer,options){var oldOnClick;options=options||{};this.trackingClick=false;this.trackingClickStart=0;this.targetElement=null;this.touchStartX=0;this.touchStartY=0;this.lastTouchIdentifier=0;this.touchBoundary=options.touchBoundary||10;this.layer=layer;this.tapDelay=options.tapDelay||200;this.tapTimeout=options.tapTimeout||700;if(FastClick.notNeeded(layer)){return}function bind(method,context){return function(){return method.apply(context,arguments)}}var methods=["onMouse","onClick","onTouchStart","onTouchMove","onTouchEnd","onTouchCancel"];var context=this;for(var i=0,l=methods.length;i<l;i++){context[methods[i]]=bind(context[methods[i]],context)}if(deviceIsAndroid){layer.addEventListener("mouseover",this.onMouse,true);layer.addEventListener("mousedown",this.onMouse,true);layer.addEventListener("mouseup",this.onMouse,true)}layer.addEventListener("click",this.onClick,true);layer.addEventListener("touchstart",this.onTouchStart,false);layer.addEventListener("touchmove",this.onTouchMove,false);layer.addEventListener("touchend",this.onTouchEnd,false);layer.addEventListener("touchcancel",this.onTouchCancel,false);if(!Event.prototype.stopImmediatePropagation){layer.removeEventListener=function(type,callback,capture){var rmv=Node.prototype.removeEventListener;if(type==="click"){rmv.call(layer,type,callback.hijacked||callback,capture)}else{rmv.call(layer,type,callback,capture)}};layer.addEventListener=function(type,callback,capture){var adv=Node.prototype.addEventListener;if(type==="click"){adv.call(layer,type,callback.hijacked||(callback.hijacked=function(event){if(!event.propagationStopped){callback(event)}}),capture)}else{adv.call(layer,type,callback,capture)}}}if(typeof layer.onclick==="function"){oldOnClick=layer.onclick;layer.addEventListener("click",function(event){oldOnClick(event)},false);layer.onclick=null}}var deviceIsWindowsPhone=navigator.userAgent.indexOf("Windows Phone")>=0;var deviceIsAndroid=navigator.userAgent.indexOf("Android")>0&&!deviceIsWindowsPhone;var deviceIsIOS=/iP(ad|hone|od)/.test(navigator.userAgent)&&!deviceIsWindowsPhone;var deviceIsIOS4=deviceIsIOS&&(/OS 4_\d(_\d)?/).test(navigator.userAgent);var deviceIsIOSWithBadTarget=deviceIsIOS&&(/OS [6-7]_\d/).test(navigator.userAgent);var deviceIsBlackBerry10=navigator.userAgent.indexOf("BB10")>0;FastClick.prototype.needsClick=function(target){switch(target.nodeName.toLowerCase()){case"button":case"select":case"textarea":if(target.disabled){return true}break;case"input":if((deviceIsIOS&&target.type==="file")||target.disabled){return true}break;case"label":case"iframe":case"video":return true}return(/\bneedsclick\b/).test(target.className)};FastClick.prototype.needsFocus=function(target){switch(target.nodeName.toLowerCase()){case"textarea":return true;case"select":return !deviceIsAndroid;case"input":switch(target.type){case"button":case"checkbox":case"file":case"image":case"radio":case"submit":return false}return !target.disabled&&!target.readOnly;default:return(/\bneedsfocus\b/).test(target.className)}};FastClick.prototype.sendClick=function(targetElement,event){var clickEvent,touch;if(document.activeElement&&document.activeElement!==targetElement){document.activeElement.blur()}touch=event.changedTouches[0];clickEvent=document.createEvent("MouseEvents");clickEvent.initMouseEvent(this.determineEventType(targetElement),true,true,window,1,touch.screenX,touch.screenY,touch.clientX,touch.clientY,false,false,false,false,0,null);clickEvent.forwardedTouchEvent=true;targetElement.dispatchEvent(clickEvent)};FastClick.prototype.determineEventType=function(targetElement){if(deviceIsAndroid&&targetElement.tagName.toLowerCase()==="select"){return"mousedown"}return"click"};FastClick.prototype.focus=function(targetElement){var length;if(deviceIsIOS&&targetElement.setSelectionRange&&targetElement.type.indexOf("date")!==0&&targetElement.type!=="time"&&targetElement.type!=="month"){length=targetElement.value.length;targetElement.setSelectionRange(length,length)}else{targetElement.focus()}};FastClick.prototype.updateScrollParent=function(targetElement){var scrollParent,parentElement;scrollParent=targetElement.fastClickScrollParent;if(!scrollParent||!scrollParent.contains(targetElement)){parentElement=targetElement;do{if(parentElement.scrollHeight>parentElement.offsetHeight){scrollParent=parentElement;targetElement.fastClickScrollParent=parentElement;break}parentElement=parentElement.parentElement}while(parentElement)}if(scrollParent){scrollParent.fastClickLastScrollTop=scrollParent.scrollTop}};FastClick.prototype.getTargetElementFromEventTarget=function(eventTarget){if(eventTarget.nodeType===Node.TEXT_NODE){return eventTarget.parentNode}return eventTarget};FastClick.prototype.onTouchStart=function(event){var targetElement,touch,selection;if(event.targetTouches.length>1){return true}targetElement=this.getTargetElementFromEventTarget(event.target);touch=event.targetTouches[0];if(deviceIsIOS){selection=window.getSelection();if(selection.rangeCount&&!selection.isCollapsed){return true
}if(!deviceIsIOS4){if(touch.identifier&&touch.identifier===this.lastTouchIdentifier){event.preventDefault();return false}this.lastTouchIdentifier=touch.identifier;this.updateScrollParent(targetElement)}}this.trackingClick=true;this.trackingClickStart=event.timeStamp;this.targetElement=targetElement;this.touchStartX=touch.pageX;this.touchStartY=touch.pageY;if((event.timeStamp-this.lastClickTime)<this.tapDelay){event.preventDefault()}return true};FastClick.prototype.touchHasMoved=function(event){var touch=event.changedTouches[0],boundary=this.touchBoundary;if(Math.abs(touch.pageX-this.touchStartX)>boundary||Math.abs(touch.pageY-this.touchStartY)>boundary){return true}return false};FastClick.prototype.onTouchMove=function(event){if(!this.trackingClick){return true}if(this.targetElement!==this.getTargetElementFromEventTarget(event.target)||this.touchHasMoved(event)){this.trackingClick=false;this.targetElement=null}return true};FastClick.prototype.findControl=function(labelElement){if(labelElement.control!==undefined){return labelElement.control}if(labelElement.htmlFor){return document.getElementById(labelElement.htmlFor)}return labelElement.querySelector("button, input:not([type=hidden]), keygen, meter, output, progress, select, textarea")};FastClick.prototype.onTouchEnd=function(event){var forElement,trackingClickStart,targetTagName,scrollParent,touch,targetElement=this.targetElement;if(!this.trackingClick){return true}if((event.timeStamp-this.lastClickTime)<this.tapDelay){this.cancelNextClick=true;return true}if((event.timeStamp-this.trackingClickStart)>this.tapTimeout){return true}this.cancelNextClick=false;this.lastClickTime=event.timeStamp;trackingClickStart=this.trackingClickStart;this.trackingClick=false;this.trackingClickStart=0;if(deviceIsIOSWithBadTarget){touch=event.changedTouches[0];targetElement=document.elementFromPoint(touch.pageX-window.pageXOffset,touch.pageY-window.pageYOffset)||targetElement;targetElement.fastClickScrollParent=this.targetElement.fastClickScrollParent}targetTagName=targetElement.tagName.toLowerCase();if(targetTagName==="label"){forElement=this.findControl(targetElement);if(forElement){this.focus(targetElement);if(deviceIsAndroid){return false}targetElement=forElement}}else{if(this.needsFocus(targetElement)){if((event.timeStamp-trackingClickStart)>100||(deviceIsIOS&&window.top!==window&&targetTagName==="input")){this.targetElement=null;return false}this.focus(targetElement);this.sendClick(targetElement,event);if(!deviceIsIOS||targetTagName!=="select"){this.targetElement=null;event.preventDefault()}return false}}if(deviceIsIOS&&!deviceIsIOS4){scrollParent=targetElement.fastClickScrollParent;if(scrollParent&&scrollParent.fastClickLastScrollTop!==scrollParent.scrollTop){return true}}if(!this.needsClick(targetElement)){event.preventDefault();this.sendClick(targetElement,event)}return false};FastClick.prototype.onTouchCancel=function(){this.trackingClick=false;this.targetElement=null};FastClick.prototype.onMouse=function(event){if(!this.targetElement){return true}if(event.forwardedTouchEvent){return true}if(!event.cancelable){return true}if(!this.needsClick(this.targetElement)||this.cancelNextClick){if(event.stopImmediatePropagation){event.stopImmediatePropagation()}else{event.propagationStopped=true}event.stopPropagation();event.preventDefault();return false}return true};FastClick.prototype.onClick=function(event){var permitted;if(this.trackingClick){this.targetElement=null;this.trackingClick=false;return true}if(event.target.type==="submit"&&event.detail===0){return true}permitted=this.onMouse(event);if(!permitted){this.targetElement=null}return permitted};FastClick.prototype.destroy=function(){var layer=this.layer;if(deviceIsAndroid){layer.removeEventListener("mouseover",this.onMouse,true);layer.removeEventListener("mousedown",this.onMouse,true);layer.removeEventListener("mouseup",this.onMouse,true)}layer.removeEventListener("click",this.onClick,true);layer.removeEventListener("touchstart",this.onTouchStart,false);layer.removeEventListener("touchmove",this.onTouchMove,false);layer.removeEventListener("touchend",this.onTouchEnd,false);layer.removeEventListener("touchcancel",this.onTouchCancel,false)};FastClick.notNeeded=function(layer){var metaViewport;var chromeVersion;var blackberryVersion;var firefoxVersion;if(typeof window.ontouchstart==="undefined"){return true}chromeVersion=+(/Chrome\/([0-9]+)/.exec(navigator.userAgent)||[,0])[1];if(chromeVersion){if(deviceIsAndroid){metaViewport=document.querySelector("meta[name=viewport]");if(metaViewport){if(metaViewport.content.indexOf("user-scalable=no")!==-1){return true}if(chromeVersion>31&&document.documentElement.scrollWidth<=window.outerWidth){return true}}}else{return true}}if(deviceIsBlackBerry10){blackberryVersion=navigator.userAgent.match(/Version\/([0-9]*)\.([0-9]*)/);if(blackberryVersion[1]>=10&&blackberryVersion[2]>=3){metaViewport=document.querySelector("meta[name=viewport]");if(metaViewport){if(metaViewport.content.indexOf("user-scalable=no")!==-1){return true
}if(document.documentElement.scrollWidth<=window.outerWidth){return true}}}}if(layer.style.msTouchAction==="none"||layer.style.touchAction==="manipulation"){return true}firefoxVersion=+(/Firefox\/([0-9]+)/.exec(navigator.userAgent)||[,0])[1];if(firefoxVersion>=27){metaViewport=document.querySelector("meta[name=viewport]");if(metaViewport&&(metaViewport.content.indexOf("user-scalable=no")!==-1||document.documentElement.scrollWidth<=window.outerWidth)){return true}}if(layer.style.touchAction==="none"||layer.style.touchAction==="manipulation"){return true}return false};FastClick.attach=function(layer,options){return new FastClick(layer,options)};if(typeof define==="function"&&typeof define.amd==="object"&&define.amd){define(function(){return FastClick})}else{if(typeof module!=="undefined"&&module.exports){module.exports=FastClick.attach;module.exports.FastClick=FastClick}else{window.FastClick=FastClick}}}());

/**https://github.com/pinceladasdaweb/isMobile*Copyright 2013 Pedro Rogerio*Licensed under the MIT license**/
var isMobile = (function (userAgent) {
  'use strict';
  return !!userAgent.match(/android|webos|ip(hone|ad|od)|opera (mini|mobi|tablet)|iemobile|windows.+(phone|touch)|mobile|fennec|kindle (Fire)|Silk|maemo|blackberry|playbook|bb10\; (touch|kbd)|Symbian(OS)|Ubuntu Touch/i);
}(navigator.userAgent));

/**
 * 响应页面窗口调整
 * @constructor
 */
function HandleResponsiveOnResize(){
    HandleSidebarAndContentHeight();
	InitImageNav();
    $(window).resize(function(){
        HandleSidebarAndContentHeight();
		//绑定或解绑滑动侧边栏事件
        //swipeToggle();
        
        //绑定移动端 Ajax 翻页事件
        BingLoadNextPageEvent($('#loadNextPageBtn'));
        
        //初始化并绑定 PC 端图片翻页
        InitImageNav();
    });

    $(window).scroll(function(){

        if($(document).scrollTop()>50)
        {
            $('#back-to-top').css({'display':'block'});
        }
        else
        {
            $('#back-to-top').css({'display':'none'});
        }
    });
}
// let weixin = document.getElementsByClassName('bds_weixin')[0];
// let dialog = document.getElementById('bdshare_weixin_qrcode_dialog');
// weixin.onclick = function(){
//     if(!$('#bdshare_weixin_qrcode_dialog_qr')[0].children.length)
//     {
//         $('#bdshare_weixin_qrcode_dialog_qr').qrcode({width:220,height: 205,text:window.location.origin+window.location.pathname})
//     }
    
//     dialog.style.display = 'block';
// };
// let popup_close = document.getElementsByClassName('bd_weixin_popup_close')[0];
// popup_close.onclick = function(){
//     dialog.style.display = 'none';
// }
/**
 * 调整返回顶部按钮的位置
 * @constructor
 */
function HandleSidebarAndContentHeight(){
    var cWidth = $('.container').width();
    var wWidth = $(window).width();
    var right = (wWidth-cWidth)/2-58;
    $('#side-fixed-button').css({right:right>10?right:10});
}

/**
 * 专题列表
 * @param id
 */
function cm_selected(id){
    var obj = $(id).find('li');
    obj.hover(function(){obj.removeClass('selected');$(this).addClass('selected')},function(){});
	obj.first().addClass('selected');
}


/**
 * 初始化侧边栏子目录
 */
function initSideMenu()
{
    $('.side-menu li.parent > a').click(function () {
        var obj = $(this).parent();
        var active = obj.hasClass('open');
        obj.parent().find('li.open').removeClass('open');
        if(!active)
            obj.addClass('open');
    });
}

/**
 * 显示或隐藏侧边栏
 * @param menu  node 侧边栏节点
 */
function sideMenuToggle(menu)
{
    if(menu.hasClass('active'))
    {
        showSideMenu(menu);
    }
    else
    {
        hiddenSideMenu(menu);
    }
}

/**
 * 显示侧边栏
 * @param menu  node 侧边栏节点
 */
function showSideMenu(menu)
{
    $('body,html').css({'overflow-y':'hidden'});
    $('.screen-cover').show();
    menu.addClass('active');
}

/**
 * 隐藏侧边栏
 * @param menu  node 侧边栏节点
 */
function hiddenSideMenu(menu)
{
    $('.screen-cover').hide();
    $('body,html').css({'overflow-y':'auto'});
    menu.removeClass('active');
}

/**
 * 显示和隐藏分享组件
 * @param menu  node 侧边栏节点
 */
function shareTo()
{
    $('body,html').css({'overflow-y':'hidden'});
    $('.screen-cover').show();
    $('#share-to').addClass('active');
}
function hideShareTo(){
	$('.screen-cover').hide();
    $('body,html').css({'overflow-y':'auto'});
     $('#share-to').removeClass('active');
}

/**
 * 平滑滚动至顶部
 */
function backToTop(){
    $("html,body").animate({scrollTop: 0}, 200);
}

/**
 * 获取滚动条距底部的距离
 * @returns {{toTop: (*|jQuery), toBottom: number}}
 */
function getScrollPositionOfBottom()
{
    var documentHeight = $(document).height();
    var scrollHeight = $(document).scrollTop();
    var widowHeight = document.documentElement.clientHeight;
    return {toTop:scrollHeight,toBottom:documentHeight-scrollHeight-widowHeight};
}

/**
 * 获取分页信息
 * @returns {{totalpagenumber: string, baselink: string}}
 * @constructor
 */
function GetPageInfo(){
    var _return={totalpagenumber:0,baselink:"#",extend:'',index:1}
    var pagelink = $('#displaypagenum').find('a');
    if(pagelink.length)
    {
        var TotalPageNum,extend,lastHref,temp;
        lastHref = pagelink.last().attr('href');
        extend = lastHref.match(/\.[a-zA-Z]+$/ig);
		temp = lastHref.substr(0,lastHref.length-extend[0].length);
		temp = temp.split("_");
		TotalPageNum = temp[1] ? temp[1] : 2;
		_return.totalpagenumber=parseInt(TotalPageNum);
        // console.log(temp, extend)
		_return.baselink= temp[0];
		_return.extend = extend[0];
        _return.index = parseInt($('#displaypagenum').find('span.page').first().text());
		
        //TotalPageNum = lastHref.match(/\d+\.[a-zA-Z]+$/ig);
        //TotalPageNum = TotalPageNum[0].substr(0,TotalPageNum[0].length-extend[0].length);
		//_return.baselink=pagelink.last().attr('href').substr(0,pagelink.last().attr('href').length-extend[0].length-TotalPageNum.length-1);
    }else{
        //预览状态的页码通过分页符获取
        var hrNum = $('#sourceHTML').find('hr').length;
        _return.totalpagenumber= hrNum ? hrNum : 1;
        _return.baselink = 'localhost';
    }
    return _return;
}

/**
 * Ajax 加载下一页数据
 * @param pageInfo
 * @param loadNextPageBtn
 * @constructor
 */
function LoadPage(pageInfo,loadNextPageBtn){
    var baseLink = pageInfo.baselink;
    var totalPageNum = pageInfo.totalpagenumber;
    var currentPage = parseInt(loadNextPageBtn.attr('data-CurrentPage'));
    var nextPage =  currentPage+1;
    var extend = pageInfo.extend;

    if(nextPage <= totalPageNum)
    {
        var pageUrl = totalPageNum == 1 ? baseLink + extend : baseLink + "_" + nextPage + extend;
        var ajaxResult = '';

        $.ajax({
            url:pageUrl,
            type:'GET',
            success:function(data){
                //取出页面中的正文部分
                ContentHtml_Reg = new RegExp("<!--HTMLBOX-->([\\s\\S]+)<!--HTMLBOX-->","i");
                ajaxResult = data.match(ContentHtml_Reg);
                //ajaxResult = ajaxResult[1].replace(/<!--[\w\W\r\n]*?-->/gmi,"");
				ajaxResult = ajaxResult[1].replace(/<!--.*?-->/gmi,"");
                ajaxResult = ajaxResult.replace(/<([^\s>]+)[^>]*>(\s*)<\/\1>/gmi,"");
                $('#article-content').append('<hr/><small class="pageNum">第'+nextPage+'页</small>'+ajaxResult);
				
				init_cm_player();

				loadNextPageBtn.attr({'data-CurrentPage':nextPage});
                if(nextPage == totalPageNum)
                {
                    // loadNextPageBtn.remove();
                    showArticleEnd()
                }
                else
                {
                    
                    $('#VProgress').text(nextPage+'/'+pageInfo.totalpagenumber);
                }
            },
			complete:function(){window.isLoadingNewPage = false;}
        });
    }
    else
    {
        // loadNextPageBtn.remove();
        return;
    }

}

/**
 * 显示页脚和相关稿件
 */
function showArticleEnd()
{
    $('#pageFooter').show();
}

/**
 * 隐藏页脚和相关稿件
 */
function hiddenArticleEnd()
{
    $('#pageFooter').hide();
}

/**
 * 绑定分页按钮事件
 * @param loadNextPageBtn
 * @constructor
 */
function BingLoadNextPageEvent(loadNextPageBtn)
{
    if($(window).width()>992)
    {
        showArticleEnd();
        return;
    }

    if(loadNextPageBtn.length>0)
    {
        hiddenArticleEnd()
    }


    if(window.NextPageBtnHasEvent)
    {
        return ;
    }

    //if(isIE5 || isIE6 || isIE7 || isIE8) return;

    var pageInfo = GetPageInfo();

    if(pageInfo.totalpagenumber>1){
        hiddenArticleEnd();
        loadNextPageBtn.click(function () {
            LoadPage(pageInfo,loadNextPageBtn);
        });
		
		$(window).scroll(function(){
			if(getBottomToView()<30){
				if(window.isLoadingNewPage)	return;
				window.isLoadingNewPage = true;
				LoadPage(pageInfo,loadNextPageBtn);
			}
		})
		
        $('#VProgress').text(1+'/'+pageInfo.totalpagenumber);
        window.NextPageBtnHasEvent = 1;
    }else
    {
        showArticleEnd();
        // loadNextPageBtn.remove();
    }
}


function getBottomToView(){
	var height = $(document).height();
	var scrollTop = $(document).scrollTop();
	var windowHeith = $(window).height();
	
	return height - scrollTop - windowHeith;
}

function BindSwipe(){
    var sideMenu = $('#side-menu,#side-menu li');
    $('html').swipe({
        swipeRight: function () {
            showSideMenu(sideMenu);
        },
        threshold:230
    });
    sideMenu.swipe({
        swipeLeft: function () {
            hiddenSideMenu(sideMenu);
        },
        threshold:70
    });
}

function swipeToggle()
{
    if($(window).width()>992)
    {
        $("html").swipe("disable");
    }
    else
    {
        $('html').swipe('enable');
    }
}
/**
 * 字符串替换函数
 * @param s1
 * @param s2
 * @returns {string}
 */
String.prototype.replaceAll = function(s1,s2) {
    return this.replace(new RegExp(s1,"gm"),s2);
}

/**
 * 在整个当前文档中找出正文图片
 * action = list 		返回数组，内容为正文图片
 * action = default	返回img对象，内容为第一张正文图片
 */
function getContentImage(action){		
	var ImgObjArr = $('img[data-id]');
	var imglist = new Array();
	if(ImgObjArr.length>0)
	{
		var CurImgID = "";
		var reg = /^\d+$/;		//判断图片ID属性的正则
		for(var i =0;i<ImgObjArr.length;i++)
		{
			CurImgID=ImgObjArr.eq(i).attr('data-id');
			if(reg.test(CurImgID)){
				imglist.push(ImgObjArr.eq(i));
			}
		}
		return action=="list" ? imglist : imglist[0];
	}
	else
	{
		return ImgObjArr;
	}
}

/**
 * 设置鼠标样式
 * img      要处理的图片信息
 * e        鼠标的事件信息
 */
function bindImageLink(img,e) {
    var imgWidth = img.width();
    var imgBox = img.parent();
    if(imgWidth/2-e.offsetX>0)
    {
        if(imgBox.hasClass('cursor-left'))
            return;        
        imgBox.removeClass('cursor-right'); 
        imgBox.addClass('cursor-left');  
        
    }
    else
    {
        if(imgBox.hasClass('cursor-right'))
            return;  
        imgBox.removeClass('cursor-left');
        imgBox.addClass('cursor-right');
    }
}

/**
 * 绑定翻页链接
 * pageinfo 分页信息
 * img      要处理的图片信息
 * e        鼠标在的事件信息
 */
function bindImageClick(LinkInfo,img,e) {
    var imgWidth = img.width();
    if(imgWidth/2-e.offsetX>0)
    {
        if(LinkInfo.pre != null)
            window.location=LinkInfo.pre;
    }
    else
    {
        if(LinkInfo.next != null)
            window.location=LinkInfo.next;
    }
}

/**
 * 计算当前页面的上下页链接
 * pageinfo     当前页面的上下文信息  getPageInfo()
 */
function getLinkOfNextAndPrePage(pageinfo)
{
    var preLink = "",nextLink="";
    // console.log(pageinfo)
    var preNumber = pageinfo.index-1>0?pageinfo.index-1:null;
    var nextnumber = pageinfo.index+1>pageinfo.totalpagenumber?null:pageinfo.index+1;
    // console.log(pageinfo, preNumber)
    preLink = preNumber==null?null:(preNumber==1?pageinfo.baselink+pageinfo.extend:pageinfo.baselink+'_'+preNumber+pageinfo.extend);    
    nextLink = nextnumber==null?null:pageinfo.baselink+'_'+nextnumber+pageinfo.extend;

    return {next:nextLink,pre:preLink}
}

/**
 * 在图片上增加翻页链接
 * 
 */
function InitImageNav()
{    
    var ContentImage = getContentImage();    
    var pageInfo;
    if($(window).width()<992)
    {
        $(ContentImage[0]).off();
        return ;
    }
    
    pageInfo = GetPageInfo();
        
    if(pageInfo.totalpagenumber <=1 )
    return;
    
    if(ContentImage.length==0)
    return;
    
    var LinkOfNextAndPrePage = getLinkOfNextAndPrePage(pageInfo);
    //bind the mousemove event on Image
    $(ContentImage[0]).mousemove(function(e){
        bindImageLink($(this),e);
    });
    $(ContentImage[0]).click(function(e){
        bindImageClick(LinkOfNextAndPrePage,$(this),e);
        
    });
    $(ContentImage[0]).mouseout(function(){
        $(this).parent().removeClass('cursor-right');
        $(this).parent().removeClass('cursor-left');
    })
}

/*CMVIDEO*/
function createHTML5video(videoUrl,ext,width,height){

	var html5video = '<video class="cm-video" controls preload="none" width="'+width+'" height="'+height+'" style="width:'+width+'px; height:'+height+'px" src="'+videoUrl+'">';
	html5video += '<source src="'+ videoUrl +'" type=\'video/'+ext+'\' /></video>';
		
	return html5video;
}

function createHTML5audio(audioUrl){
	return '<audio class="cm-audio" controls autoplay preload="none" src="'+audioUrl+'"></audio>'
}

function createEmbedAudio(mediaUrl){
	return '<embed type="audio/mp3" src="'+mediaUrl+'"  height="45" width="280" autostart=true loop=false></embed>'
}

function createFlash(flashvar,width, height){
	var FlashPlayer = '<object codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,29,0" ';
	FlashPlayer += 'width="'+width+'" height="'+height+'" classid="clsid:D27CDB6E-AE6D-11cf-96B8-444553540000">';
	FlashPlayer += '<param name="movie" value="http://tv.81.cn/quote/24310.files/player.swf">';
	FlashPlayer += '<param name="quality" value="high">';
	FlashPlayer += '<param name="allowFullScreen" value="true">';
	FlashPlayer += '<param name="FlashVars" value="'+ flashvar +'">';
	FlashPlayer += '<embed id="cmplayer_video" pluginspage="http://www.macromedia.com/go/getflashplayer" width="100%" height="'+height+'" quality="high" ';
	FlashPlayer += 'src="http://tv.81.cn/quote/24310.files/player.swf" flashvars="'+ flashvar +'" allowfullscreen="true" type="application/x-shockwave-flash">';
	FlashPlayer += '</object>';
	return FlashPlayer;
}

function makeFlashVars(videoUrl){
	var flashvars = [
		'name=八一电视',
		'link=http://tv.81.cn',
		'link_target=_blank',
		'share_cmp=0',
		'context_menu=false',
		'skin_info=0',
		'api=cmp_loaded',
		'src='+videoUrl,
		'mixer_filter=1',
		'mixer_id=5',
		'label=name',
		'skin=http://tv.81.cn/quote/24310.files/vplayer.swf',
		'auto_play=1',
		'config=0',
		'fullscreen_scale=1',
		'video_scalemode=1',
		'sound_sample=true'
	];
	return flashvars.join('&');
}
function IsSupportHTML5(){
	
	if(!!document.createElement('video').canPlayType)
	{
		return true;
	}else{
		return false;
	}
}

function getFileExt(filePath){
	var re = /(\\+)/g;
	var filename=filePath.replace(re,"#");
	var one=filename.split("#");
	var two=one[one.length-1];
	var three=two.split(".");
	var ext=three[three.length-1];
	return ext.toLowerCase();
}

/**
 * 读取页面中所有的媒体链接信息
 * 
 * @returns 媒体信息清单
 */
// function getMediaInfo() {
// 	var scripts = $('script[title]');
// 	var list = [];
// 	var linkto = ['Myzaker'];
// 	var url = null;
// 	var _str = null;
	
// 	for (var i = 0; i < scripts.length; i++) {

// 		_str = scripts[i].text.trim();
// 		_str = _str.replaceAll('\n','');
// 		_str = _str.replaceAll('<!--','');
// 		_str = _str.replaceAll('-->','');
// 		_str = _str.trim();


// 		url = _str.split(' ');
// 		url.length < 2 && (url = _str.split('|'));

// 		list.push({
// 			script: scripts[i],
// 			type: url[0].trim().substr(2),
// 			mediaUrl: url[1].trim(),
// 			ext:getFileExt(url[1].trim()),
// 			linkto:linkto.indexOf(url[0].trim().substr(2))>=0
// 		})

// 	}

// 	return list;
// }

//增加trim
if(typeof String.prototype.trim !== 'function') {
	String.prototype.trim = function() {
		return this.replace(/^\s+|\s+$/g, ''); 
	}
}

//添加数组IndexOf方法
if (typeof Array.prototype.indexOf !== 'function'){
  Array.prototype.indexOf = function(elt /*, from*/){
    var len = this.length >>> 0;

    var from = Number(arguments[1]) || 0;
    from = (from < 0)
         ? Math.ceil(from)
         : Math.floor(from);
    if (from < 0)
      from += len;

    for (; from < len; from++){
      if (from in this && this[from] === elt)
        return from;
    }
    return -1;
  };
}

var resizer = {};

resizer.bind = function (element){
	$(window).resize(function(){
		var Size = getVideoSize();
		element.css({width:Size.width,height:Size.height});
		element.attr({width:Size.width,height:Size.height});
	})
}

function getVideoSize(){
	var videoWidth = $('#cm-player').width();
	videoWidth = videoWidth >800 ? 800 : videoWidth

	return {
		width:videoWidth,
		height:Math.ceil(videoWidth*0.56255)
	}
}

function init_cm_player(){
	
	var VideoSize = getVideoSize();
	var videoWidth = VideoSize.width;
	var videoHeight = VideoSize.height;	
	var medias = $('video').length ? $('video') : $('audio');
    var issupporthtml5 = IsSupportHTML5();
	var _media = null;
	var mediaId = window.mediaID;
	for(var i = 0; i<medias.length; i++){
		window.mediaID++;
		_media = medias[i];
		switch (_media.tagName){

			case 'VIDEO':
				if (issupporthtml5) {
                    _media.style = 'width:' + videoWidth + 'px;height:' + videoHeight + 'px;';
                    console.log(_media.style, videoWidth, videoHeight);
				}else{
					$(_media.script).replaceWith('<div id="video-'+mediaId+'" class="cm-player">'+createFlash(makeFlashVars(_media.mediaUrl), videoWidth, videoHeight)+"</div>");
				}
				
				resizer.bind($('#video-'+mediaId + ' video'));
			break;

			// case 'AUDIO':
			// 	if (issupporthtml5) {
			// 		$(_media.script).replaceWith('<div id="audio-'+mediaId+'" class="cm-player">'+createHTML5audio(_media.mediaUrl)+"</div>");
			// 	}else{
			// 		$(_media.script).replaceWith('<div id="audio-'+mediaId+'" class="cm-player">'+createEmbedAudio(_media.mediaUrl)+"</div>");
			// 	}
			// 	$('#audio-'+mediaId).css({'margin-left':'0'})
			// break;

			//如果是微场景
			case 'Scene':
				_scenename = MSSupport(_media.mediaUrl);
				if (_scenename) {
					if (_media.mediaUrl.length < 10) {						
						break;
					}

					if (isMobile) {
						window.location = _media.mediaUrl;
					}					
					else 
					{
						$('#qrCode').remove();
						createMobileBox(_media,_scenename);
						return;
					}    
				}
			break;
		}
	}
}
/*视频播放器结束*/

$().ready(function(){
    var sideMenu = $('#side-menu');

    // 绑定窗口变化事件
    HandleResponsiveOnResize();

    //初始化侧边栏子目录
    initSideMenu();

    //初始化 Ajax 翻页
    // BingLoadNextPageEvent($('#loadNextPageBtn'));

    //初始化专题切换
    cm_selected('.list_topic_toggle');

	
    //绑定呼出、隐藏侧边栏事件
    //BindSwipe();
	//启用和禁用 swipe 组件
    //swipeToggle();
    //$('.close-side-menu').click(function () {hiddenSideMenu(sideMenu)});
    //$('.showSideMenu').click(function () {showSideMenu(sideMenu)});
	
	$('.screen-cover').click(function(){hideShareTo()});

    //300毫秒
    $(function() {
        FastClick.attach(document.body);
    });

    /*二维码*/
    if($('#qrCode').qrcode)
    {
        $('#qrCode').qrcode({width:115,height: 115,text:window.location.origin+window.location.pathname});
    }
	
	//加载播放器
	init_cm_player();

}());

$(function(){
	var tbox = null;
	if($(document).height()<1300){
		$('.toggle').text('展开');
	}else{
		$('.toggle').text('隐藏');
		$('.toggle-box').addClass('show');
	}
	
	$('.toggle').click(function(){
		tbox = $(this).parents('.toggle-box');
		if(tbox.hasClass('show')){
			tbox.removeClass('show');
			$(this).text('展开');
		} else {
			tbox.addClass('show');
			$(this).text('隐藏');
		}
	});
})

+function(){
	var url = '',ext = '';
	var pathname = window.location.pathname.split('/');
	var filename = pathname[pathname.length-1].split('_');
	if(filename.length == 3){
		pathname.pop();
		ext = (filename.pop()).split('.');
		url = pathname.join('/')+'/'+filename.join('_')+'.'+ext[ext.length-1];
		if(isMobile){
			location.href = url;
		}
	}
	else
	{
		url = window.location.pathname;
	}
	window._bd_share_config={
		"common":{
			"bdUrl" : 'http://' + window.location.host+ '/' + url,			
			"bdSnsKey":{},
			"bdText":"",
			"bdMini":"2",
			"bdMiniList":false,
			"bdPic":"",
			"bdStyle":"1",
			"bdSize":"16"
		},
		"share":{}
	};
    let domain1 = document.getElementById('domain').content;
    console.log(domain1);
	with(document)0[(getElementsByTagName('head')[0]||body).appendChild(createElement('script')).src=domain1+'static/api/js/share.js?v=89860593.js?cdnversion='+~(-new Date()/36e5)];
}()

$('.bd_weixin_popup_close').on('click', function(){
    $('#bdshare_weixin_qrcode_dialog_bg').hide()
})



// $(function(){

// // 统计代码
//   $.ajax({
//     url: 'https://rmt-zuul.81.cn/api-traffic/web/poll?u=' + window.location.href,
//     type: 'GET',
//     success: function (res) {
//       console.log('执行点击量监控')
//     },
//     error: function (error) {},
//   })
//   if ($('.bdsharebuttonbox').length > 0) {
//     $('.bdsharebuttonbox a').on('click', function() {
//         // 分享代码
//         $.ajax({
//         url: 'https://rmt-zuul.81.cn/api-traffic/web/share?u=' + window.location.href,
//         type: 'GET',
//         success: function (res) {
//             console.log('执行分享量监控')
//         },
//         error: function (error) {},
//         })
//     })
//   }

// })

