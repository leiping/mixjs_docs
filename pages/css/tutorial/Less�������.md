

#�����ṹ�����԰汾1.3.0��

	
<ref name="2.JPG"></ref>

#����һ��������Ϊclass

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
	
	
> ����class�ᱻ�����д


#���Զ���������Ϊfunc.


����LESS��

	.baseMain(){
	    text-align:e("baseMain func");
	}

	.basePartial(){
	    text-align:e("basePartial func");
	}

ֻ��a1.less��ʹ�ã�

	@import "base";

	.a1{
	    text-align:e("a1");
	    .baseMain();
	}


��a2.less\b1.less\b2.less��û�е�����Щfunc��������
	
	@import "base";


�������ɵ�CSS�ļ����£�

	.a1{text-align:a1;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;}
	.a2{text-align:a2;}
	.a{text-align:a;}
	.b1{text-align:b1;}
	.b2{text-align:b2;}
	.b{text-align:b;}
	.c{text-align:c;}
	.output{text-align:output;}
	
���Կ���.a1����ʽ��������4��base Main func����ʽ��**������ֺ�base.less �����õĴ�����ͬ�������ں����ĵ��ô����ǲ�ͬ��**��

#����������Ӷ�base.less ���ã���֤���Զ�

���Զ���ֻ��a2.less\b1.less\b2.less������base.less��������a.less/b.less����Ӷ�base.less�����ã�Ԥ��Ӧ�û�����6��base Main func����ʽ������:

a.less

	@import "base";
	@import "a1";
	@import "a2";

	.a{
	    text-align: e("a");
	}

b.less
	
	@import "base";
	@import "b1";
	@import "b2";

	.b{
	    text-align: e("b");
	}

��������css���£�

	.a1{text-align:a1;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;}
	.a2{text-align:a2;}
	.a{text-align:a;}
	.b1{text-align:b1;}
	.b2{text-align:b2;}
	.b{text-align:b;}
	.c{text-align:c;}
	.output{text-align:output;}


�պ�6��baseMain func����Ԥ�ڡ�

#�����ģ����㺯�����ã����import

�ڲ��Զ��Ͳ���������������base.less�еĺ�������a1.less��������ֻ��import������������b.less�е���base.less�е�.basePartial()��������base.less�ĺ������ú�import��������£�

��base.less �ĵ���

a1.less
	
	@import "base";

	.a1{
	    text-align:e("a1");
	    .baseMain();
	}
	

b.less
	
	@import "base";
	@import "b1";
	@import "b2";

	.b{
	    text-align: e("b");
	    .basePartial();
	}


import  base.less ���ļ�����a1.less��b.less�⻹��b1.less��b2.less���ܹ�4���ļ���


����Ԥ�ڣ�����.basePartial()��.baseMain()�Ĵ�����base.less ��import�����Ĵ���ϢϢ��ء��������Ӧ����4.

���������£�

	.a1{text-align:a1;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;text-align:baseMain func;}
	.a2{text-align:a2;}
	.a{text-align:a;}
	.b1{text-align:b1;}
	.b2{text-align:b2;}
	.b{text-align:b;text-align:basePartial func;text-align:basePartial func;text-align:basePartial func;text-align:basePartial func;}
	.c{text-align:c;}
	.output{text-align:output;}


���Կ�������baseMain �� basePartial �ĵ��þ�Ϊ4��

#����

���Ի���lessҪ�㹻���£�һ������import�����Ĵ����ܶ��Ժ�����css�ļ���Ҳ��������Ҫ���ǣ������������ܶࡣ



