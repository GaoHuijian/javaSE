一：Swing两种容器
============
1、顶级容器
----------
	JFrame
	JApplet
	JWindow
	JDialog
####每个顶级容器定义了一系列的窗格（pane），顶部是JRootPane类型的实例。
	玻璃窗格（glass pane）
	内容窗格（content pane）
	分层窗格（layered pane）
2、轻量级容器
-----------
	JPanel
	JScrollPane
	JRootPane
二：Swing线程
==========
GUI一般在事件调度线程上创建，使用SwingUtilities类定义的两个方法：
------
	invokeLater();
	invokeAndWait();
三：常用组件
============
1、Swing按钮
------------
	JButton
	JToggleButton
	JCheckBox
	JRadioButton
2、 JLabel标签
--------
3、Icon图标
---------
	1、使用 Icon接口，必须实现 Icon 接口中的 3 个方法：
	 public int getIconHeight()
	 public int getIconWidth()
	 public void paintIcon(Component arg0, Graphics arg1, int arg2, int arg3)
	2、利用 javax.swing.ImageIcon 类根据现有图片创建图标
4  菜单栏
JButton
----------
5
----------
四：布局管理器
============
1 FlowLayout 
-----------
	FlowLayout 类中具有以下常用的构造方法：
	1 public FlowLayout()
	2 public FlowLayout(int alignment)
	3 public FlowLayout(int alignment,int horizGap,int vertGap)
		 FlowLayout.LEFT=0
		 FlowLayout.CENTER=1
		 FlowLayout.RIGHT=2
	
2 BorderLayout
------------
	在默认不指定窗体布局的情况下，Swing 组件的布局模式是边界（BorderLayout）布局管理器。

	BorderLayout.NORTH      在容器中添加组件时，组件置于顶端
	BorderLayout.SOUTH		在容器中添加组件时，组件置于底端
	BorderLayout.EAST		在容器中添加组件时，组件置于右端
	BorderLayout.WEST		在容器中添加组件时，组件置于左端
	BorderLayout.CENTER		在容器中添加组件时，组件置于中间开始填充，直到与其他组件边界连接

3 GridLayout
--------------
	网格布局管理器主要有以下两个常用的构造方法。
	public GridLayout(int rows,int columns)。
	public GridLayout(int rows,int columns,int 
4 GridBagLayout
---------------
5 SpringLayout
--------------	
6 绝对布局
--------------
	使用绝对布局的步骤如下：
	（1）使用 Component.setLayout(null)方法取消布局管理器。
	（2）使用 Component.setBounds()方法设置每个组件的大小与位置。

五：事件
========
	ActionEvent--------------------------------------ActionListen

	AdjustmentEvent----------------------------------AdjustmentListener

	FocusEvent---------------------------------------FocusListener

	ItemEvent-----------------------------------------ItemListener

	KeyEvent------------------------------------------KeyListener

	MouseEvent-----------------------------------------MouseListener 和 MouseMotionListener

	MouseWheelEvent------------------------------------MouseWheelListener

	AncestorEvent	---------------------------------

	CaretEvent	--------------------------------

	ChangeEvent	--------------------------------

	HyperlinkEvent	-----------------------------

	InternalFrameEvent---------------------------
	
	ListDataEvent	---------------------------

	ListSelectionEvent	---------------------------

	MenuDragMouseEvent	---------------------------

	MenuEvent	---------------------------

	MenuKeyEvent	---------------------------

	MouseInputAdapter	---------------------------

	PopupMenuEvent	---------------------------

	RowSorterEvent	---------------------------

	TableColumnModelEvent	---------------------------

	TableModelEvent	---------------------------

	TreeExpansionEvent	---------------------------

	TreeModelEvent	---------------------------

	TreeSelectionEvent	---------------------------

	UndoableEditEvent---------------------------

适配器类
===========