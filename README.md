# actividad-1-lista-
posicionar el actual, eliminar el primero de la lista buscar elemento de la # Metodo para posicionar el actual

	def pos_actual (self , posicion ):
		if (self.__n == 0 or posicion > self.__pos):
			return
		nodo=self.__primero
		for i in range (self.__n):
			if (i==posicion):
				self.__actual=nodo
				return self.__actual.info
			nodo=nodo.sig


	# Metodo para buscar el elemento
	def buscar_elem (self , valor ):
		if (self.__n==0):
			return
		nodo = self.__primero
		for i in range (self.__pos+1):
			if (nodo.info != valor):
				nodo=nodo.sig
			else:
	
				return nodo.info , i 

	# Metodo para elimiar el primero de la lista 
	def eliminar_primero(self):
		if(self.__primero==None):
			return
		nodo=self.__primero
'''Para mi esta es la parte que le falta a el código ya que cuando elimine a el lugar donde apunta el actual el sigue apuntando en esa dirección y necesita ser movido '''
		if (self.__actual == nodo):
			self.__actual == nodo.sig
		self.__primero=nodo.sig
		self.__n = self.__n-1
		self.__pos = self.__pos-1
		del nodo
		if(self.__n==0):
			self.__ultimo=None
			self.__actual=None
