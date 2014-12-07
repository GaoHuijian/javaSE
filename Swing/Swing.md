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
	JRootPane
二：Swing线程
==========
GUI一般在事件调度线程上创建，使用SwingUtilities类定义的两个方法：
------
	invokeLater();
	invokeAndWait();
三：常用组件
============
1，Swing按钮
-------
	JButton
	JToggleButton
	JCheckBox
	JRadioButton
2
--------
3
---------
4
----------
5
----------
四：布局管理器
============
1 FlowLayout 
-----------
	
2 BoardLayout
------------
3 GridLayout
--------------
4 GridBagLayout
---------------
5 SpringLayout
--------------	
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