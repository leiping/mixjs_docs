#�򣨳������£�

##�ļ���֯
less�ļ����������֣������ļ���֯�Ƕȿ��ǣ�

+ ����
+ class

������Ϊ��

+ �������������������ڲ����еĺ�����
+ ͨ�á��������ȡ�����������֮�����ʹ�á�

class��Ϊ��

+ �������ⲿ��class�ṩ������������ʽ����չʾ��
+ ��չ���ⲿ��class���ڶ��ƣ���ҵ���п�������ඨ�ƵĲ��֣����Button���ϼ�ͷ��ͻ�ƻ�����ʽ������չclass��ʽչ�֡�

#��֮ǰ������

����Ҫ�ļ�������ָ�꣺����ԣ�����չ�ԣ���ά���ԡ�


##h5

	1.����class��ǩ��
	2.������DOM�ṹ�����Ƚϸߣ�
	3.�ܵ������ռ�#tbh5v0��
	4.ʵ�ַ�ʽ������⣻
	5.ҵ������ȸ�:����˵ҳβ��Less�ṹ��
	.footer{
		a{
		}
		.footer-t{
			.user-info{}
			.gotop{}
			
		}
		.footer-l{
		}
		.copyright{
		}
	}
	
	6.��bootStrap�Ƚ�����H5��less�ṹ���Ի��磺���´��룺
	.c-list-sort{
		&:after{}
		li{
			&.highlight{}
			&.sort-asc, &.sort-desc  {
				label{}
				span{}
				em{
					&:first-child{}
					&:last-child{}
				}
			}
			&.sort-asc{
				em{
					&:first-child{}
					&:last-child{}
				}
			}
			&.sort-desc{
				em{
					&:first-child{}
					&:last-child{}
				}
			}
		}
		
	}
	
	�ٱ����ҳ��
	.c-pnav-con{
		a{}
		ul{
			li{}
			
		}
		.c-p-sec{
			div{}
			.tri(){
				a{}
				.c-p-p{
					em{}
				}
			}
		}
		
		.c-p-pre{}
		.c-p-next{}
		.c-p-cur{
			.c-p-arrow{
				span:first-child{}
			}
			.c-p-down{
				span:last-child{}
			}
			.c-p-up{
				span:last-child{}
			}
		}
		
		.c-p-grey{
			a{}
		}
		
		.c-p-select{}
	}
	
	�̸���ڵĽṹ������û��ʲôά���Կ��ԡ�
	
	
##TaobaoPad
	1.�����ؼ� ���������ռ䣬�ṹ��������text�ؼ���
	#c-text {	
		//�ռ��ڵĹ��ú���
		.circle(@w) {}
		.pack-text(@w: 298px, @h: 33px) {}
		
		//�ռ��ڵĻ�����ʽclass����ʽ��չ
		.c-text {}
	}
	
	//������ʽ.
	.c-XXX{}
	
	2.���ƹ��ܺ����ֲ��ڲ�ͬ�Ŀؼ��������ռ��£�����ά������ϵͣ����ȸߣ�����һ����ά�����루����ά����ʱ��Ҫά�������ͬcode��
	3.��չ����˵�����ڵ����ؼ��ڵ���func����չ�����������š�
	


##bootStrap
	
	1.��ʽ�����ڱ�ǩ�Ĺ��ܲ��֣�����inputֻ����foucs��disable��required�ȵȡ����е���Щ���Ƕ��Ǵ�input�Ĺ��ó�����
	2.�����Դ���������ıȽ϶ࡣ����������������⣬���С���ѭ��One class, multiple tags����
	3.�Ƚ��ٵ�class��ǩ���������Ԫ��ѡ������ǩ���ӹ�������˵����֮H5��ҵ����Ϻܵ�	��
	4.���ɱ����DOM�ṹ��Ҫʵ��ĳЩ������ʽ����Ҫ����Լ����DOM�ṹ��������H5�Ƚ����ơ�����Լ��ǿ����Ȼ�Ƚϵ͡�
	5.����ʽ��ȡ����func��������鷳Щ�������п��������չ�ķ��ա�

<ref name="1.JPG"></ref>

����ͼ��TaobaoPad�����ݼ����ڿؼ���bootStrap���ڳ��һ����func���й�����˿ؼ���С�ڸ����ṹ�о��Եá��ݡ��͡��֡���

**��һ�����⣺LESS�ļ��������**

�����ļ��ṹ����ͼ:

<ref name="2.JPG"></ref>

����LESS��

	.base{
	    text-align:e("base");
	}

a1.less:
	
	@import "base";

	.a1{
	    text-align:e("a1");
	}

a2.less

	@import "base";

	.a2{
	    text-align:e("a2");
	}

a.less

	@import "a1";
	@import "a2";

	.a{
	    text-align: e("a");
	}
	
b1.less

	@import "base";

	.b1{
	    text-align:e("b1");
	}

b2.less
	
	@import "base";

	.b2{
	    text-align:e("b2");
	}
	
b.less

	@import "b1";
	@import "b2";

	.b{
	    text-align: e("b");
	}
	
c.less

	@import "base";

	.c{
	    text-align:e("c");
	}
	
output.less
	
	@import "a";
	@import "b";
	@import "c";
	.output{
	    text-align:e("output");
	}

�������ɵ�CSS�ļ����£�

	.base{text-align:base;}
	.a1{text-align:a1;}
	.base{text-align:base;}
	.a2{text-align:a2;}
	.a{text-align:a;}
	.base{text-align:base;}
	.b1{text-align:b1;}
	.base{text-align:base;}
	.b2{text-align:b2;}
	.b{text-align:b;}
	.base{text-align:base;}
	.c{text-align:c;}
	.output{text-align:output;}
	
**����������ļ�����5��base.less�ļ�����������Ҫ��һ��**


�ۺϱȽϣ�����bootStrap��ͨ�ÿ⣬���л�ʹ�úܶ��ǩѡ��������from�ж�legend�Ķ��壺
	
	// Groups of fields with labels on top (legends)
	legend {
	  display: block;
	  width: 100%;
	  padding: 0;
	  margin-bottom: @baseLineHeight;
	  font-size: @baseFontSize * 1.5;
	  line-height: @baseLineHeight * 2;
	  color: @grayDark;
	  border: 0;
	  border-bottom: 1px solid #e5e5e5;

	  // Small
	  small {
	    font-size: @baseLineHeight * .75;
	    color: @grayLight;
	  }
	}

> ��ʹ�����ɶȶ��ԣ���ǩѡ������ʹ�ûή�����ɶȣ���class�����һЩ����������֪����DOM�ṹ��Ƶ�������仯��DOM�У���ǩѡ������һ��ѡ��


bootStrap�е����ַ�ʽ������һ�������ɶȡ�����Ƶ�Ҫ��ϸߡ�

#�淶��

##����

�����淶���ڿؼ�Class�����ϻ����Ϻ͹淶��������������Ҫ����һ���ġ���ʶ�ȡ���

��Accordion��carousel���������˼�Ϳؼ���ʲô������

###class ����

###��������

###��������

�����������壺�磺

	@sansFontFamily:        "Helvetica Neue", Helvetica, Arial, sans-serif;
	@btnBackground:                     @white;

##�����ʽ�淶��������Ƕȿ��ǣ�

�ⲿ����Ҫ��������ı�Ҫ���Զ��壬��ΪCore��basic��extend�������֡�

+ Core���֣�һ������ܹ�չ�ֵ�������Ĳ��֣������˵������������ܲ���������������ԣ�����Ӧ�����ʹ�õĲ��֣�����Button�ı߿�Բ�ǡ�����Щ��������Ŀʹ�ú�Ƶ����
+ basic���֣��糤��������ɫ��������ɫ����Ӱ�ȵȡ�
+ extend���֣��ⲿ�ָ���ҵ��ľ�����Ҫ��һ���ġ����ơ��ɷ֡����Button�Ӹ���ͷ��������ܾ���Ҫ�޸�Button��DOM�ṹ��������CLass��ʽר���ṩ

	
#�����������	

�˴���ʱֻ֧��webkit���ʼ���������ֻ�ڲ�ͬ��webkit�İ汾�������֮�俼�ǡ�

#�����������

������һ��������һ������ĺ���Ӧ�Ŀ�����Щ���棿

+ ����&����ԣ�һЩ�����������ͨ�õ����ԣ���һ���ֿ��Ե�����ƣ���һЩ������ĳЩ������еġ����ԡ����ⲿ�ֿ���ͨ��������ʽMixin������
+ �����ԣ�������Ҫ�ߣ���ʹ��ʱҪ��֤�����ܵķ��㡣
+ ��չ�ԣ���Կ��ܱ仯��������Ҫ����һ������չ�Ŀռ䡣�ر��ڽṹ�ϣ�����û����չ�ԡ�
+ �����ԣ���֤һЩ���ú����ıȽϺõĸ����ԣ�ά��������ȡ�

###less����������

+ ����hack

+ �����ϲ���mixin��

###������չ��

**Q��**�����һ��less function������һ������Ϊ����Ҫ��д�����ԣ������ں����Ŀ���������Ҫ������չ������δ�����
���´��룺


	.btn {
	  display: inline-block;
	  .ie7-inline-block();
	  padding: 4px 12px;
	  margin-bottom: 0; // For input.btn
	  font-size: @baseFontSize;
	  line-height: @baseLineHeight;
	  ...


**A��**�����㿴���ģ�bootstrap�ѿ��ܻ�仯�Ĳ��ֶ��ĳ��˱�����Ȼ��Ϳ������ɲ�ͬ�汾�Ŀؼ���


**Q��**���ʹ������ʹ��v0.1��ť�����
	�������СΪ14px
	���и�Ϊ18px
	��v0.2�İ汾�У���������ԭ��������и߸ĳ����£�
	�������СΪ12px
	���и�Ϊ14px
	������ĳЩ�������кܴ�����������ģ�������������С���иߣ�
	����ĳ��ʹ������ʹ��v0.1�������С����v0.2���иߣ���ô�죿����
	
**A��**�Բ��𣬰汾һ���̶������ṩ���������޸ģ��������Լ���Ӧ����Ե��޸ĸ��ǡ�


**Q��**һЩ��չ����ͨ������ʵ�֣�Ҳ����ͨ��classʵ�֣�����������֣�
**A��**��������Բ���ģ��ڰ汾�Ͱ汾֮��ı仯������class���Ƕ�ҵ�����չ��һ��������ԭ���ġ��ӡ���һ�������˺ܶࡰ�ӡ��������߶������ڰ汾�ĸ����С�


###����(tricks)

1.ͨ�����

	[class^="icon-"],
	[class*=" icon-"] {
	 	display: inline-block;


2.Mix in
	
	input[type="button"] {
	  &.btn-block {
	    width: 100%;
	  }
	}

һ��DOMԪ����CSS���ж���ѡ��ʽ��
+ class
+ ��ǩ
+ ѡ�������ϵ�����ԡ�α��ȣ�
+ ID


���ʹ�ÿ���ʵ�ֶ��ơ�


#��������

bootStrap�����¼������ֶԱ��������˻��֣�

��Ҫ���ֱ�׼��
	
	�ؼ�
	��ɫ
	�ߴ�

+ Grays
+ Accent colors(Ũɫ)
+ Scaffolding
+ Links
+ Typography
+ Component sizing��Based on 14px font-size and 20px line-height��
+ Tables
+ Buttons
+ Forms
+ Dropdowns
+ Z-index master list(COMPONENT VARIABLES)
+ Sprite icons path
+ Input placeholder text color
+ Hr border color
+ Horizontal forms & lists
+ Wells
+ Navbar
+ Pagination
+ Hero unit
+ Form states and alerts
+ Tooltips and popovers
+ GRID

#���



##Form

1.������Ĳ��֡����塢�Ű����ԡ�
2.���ɱ༭��������
3.��ý���

##Button

class

func


bootStrap����Ʒ�ʽ��ѡ���+class��
1.������ǩ��

	label,
	input,
	button,
	select,
	textarea

inputչ����

	input[type="text"],
	input[type="password"],
	input[type="datetime"],
	input[type="datetime-local"],
	input[type="date"],
	input[type="month"],
	input[type="time"],
	input[type="week"],
	input[type="number"],
	input[type="email"],
	input[type="url"],
	input[type="search"],
	input[type="tel"],
	input[type="color"]
	input[type="radio"],
	input[type="checkbox"]
	input[type="file"],
	input[type="image"],
	input[type="submit"],
	input[type="reset"],
	input[type="button"],
	input[type="checkbox"]

selectչ����
	
	select[multiple],
	select[size]

2.class������

	uneditable-input
	uneditable-textarea
	
3.DOMԼ���������

	<label class="checkbox">
	  <input type="checkbox" value="">
	  Option one is this and that��be sure to include why it's great
	</label>
	 
	<label class="radio">
	  <input type="radio" name="optionsRadios" id="optionsRadios1" value="option1" checked>
	  Option one is this and that��be sure to include why it's great
	</label>
	<label class="radio">
	  <input type="radio" name="optionsRadios" id="optionsRadios2" value="option2">
	  Option two can be something else and selecting it will deselect option one
	</label>
	
**Q:**�������class ��checkbox������radio��Ϊ��ʵ���ڲ�DOMչʾ��������ԭ����input��ǩ������һ��label,�Ƿ�Ӱ������ԣ����絥��ʹ��һ��radioButton����

**A:**��ֻ��һ����չ���������input��ǩ����ʽ�����ṩ�ģ���չCode����������չ����ΪҪ��õ�DOMչ��Ч��������DOM������չ�����£�

	.radio,
	.checkbox {
	  min-height: @baseLineHeight; // clear the floating input if there is no label text
	  padding-left: 20px;
	}
	.radio input[type="radio"],
	.checkbox input[type="checkbox"] {
	  float: left;
	  margin-left: -20px;
	}



#�����ͻ

��ǰ����ʽ��Ӧ�õ���ʽ��������ͻ�����⡣

##�����ռ�

bootStrapʹ�õ������ռ䣬��Щʹ�������ռ��func���ص�����и��߼��ϵġ���������ϵ����class���в�ͬ��ʹ�������ռ�ĺô�֮һ���ǣ�1.�Ѻõ�������֯��2.���õ���ȷ�ԡ����������Ӧ���У��᲻���Ӧ���еı�ǩ��ͻ��bootStrap��������ò�ƾ����ܹ���ˡ���

	#font {
	  #family {
	    .serif() {
	      font-family: @serifFontFamily;
	    }
	    
	...
	
	#grid {

	  .core (@gridColumnWidth, @gridGutterWidth) {

	    .spanX (@index) when (@index > 0) {
	      (~".span@{index}") { .span(@index); }
	      .spanX(@index - 1);
	    }


#��չ

��Ϊ��ʽ��չ��DOM��չ

##��ʽ��չ

��ǰ����������ʽ��չֱ�����Ӷ���class

##DOM��չ

��Ҫ�����е�������޸Ļ�������DOM�ṹ����Щ����������Ҫ���֣����һ�����֣�����ʽ��


	