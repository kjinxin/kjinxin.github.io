---
layout: post
title: PandasTable
comments: true
categories: Tools
---
## Reuse the Pandas frame from the Gui

    from tkinter import *
	  from pandastable import Table, TableModel
	  import pandas as pd

	class TestApp(Frame):
	    """Basic test frame for the table"""
	    def __init__(self, parent=None):
		self.parent = parent
		Frame.__init__(self)
		self.main = self.master
		self.main.geometry('600x400+200+100')
		self.main.title('Table app')
		f = Frame(self.main)
		f.pack(fill=BOTH,expand=1)
		self.df = df = pd.read_csv('./2.csv')
		self.table = pt = Table(f, dataframe=df,
		                        showtoolbar=True, showstatusbar=True)
		pt.show()
		return

	class TestNew(Frame):
	    """Basic test frame for the table"""
	    def __init__(self, df):
		self.parent = None
		Frame.__init__(self)
		self.main = self.master
		self.main.geometry('600x400+200+100')
		self.main.title('Table app')
		f = Frame(self.main)
		f.pack(fill=BOTH,expand=1)
		self.table = pt = Table(f, dataframe=df,
		                        showtoolbar=True, showstatusbar=True)
		pt.show()
		return

	app = TestApp()

	#launch the app
	app.mainloop()

	appnew = TestNew(app.df)
	appnew.mainloop()

We should keep the pandastable in the class, then after close the Gui, we could make our own change to the take, ex, reopen the Guiand show the table.
