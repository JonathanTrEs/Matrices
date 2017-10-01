
require "racional.rb"

class Matriz

   attr_accessor :matriz, :f, :c

    def initialize(mat) #constructor
      @matriz = mat #array de arrays con la matriz
      @f = mat.size #filas de la matriz
      @c = mat[0].size #columnas de la matriz
    end
    # Metodo para sumar dos matrices
    def +(mat)
	    resultado = Matriz.new(@matriz)
	    for i in 0...@f do
		    for j in 0...@c do
			    resultado.matriz[i][j] =@matriz[i][j] + mat.matriz[i][j]
		    end
	    end
	    resultado
    end
    # Metodo para restar dos matrices
    def -(mat)
	resultado = Matriz.new(@matriz)
	for i in 0...@f do
		for j in 0...@c do
			resultado.matriz[i][j] =@matriz[i][j] - mat.matriz[i][j]
		end
	end
	resultado
    end
    # Metodo para multiplicacion dos matrices
    def *(mat)
      if (@c == mat.f)
	aux = Array.new
	for i in 0...@f do
	  aux[i] = Array.new
	  for j in 0...mat.c do
	    if(mat.matriz[0][0].class == Fraccion)
	      aux[i][j] = Fraccion.new(0,1)
	    else
	      aux[i][j] = 0
	    end
	  end
	end
	resultado = Matriz.new(aux)
	for i in 0...@f do
	  for j in 0...mat.c do
	    for k in 0...@c do
	      resultado.matriz[i][j] += @matriz[i][k] * mat.matriz[k][j]
	    end
	  end
	end
	return resultado
    else
      puts "error"
    end
end
    
    # Metodo para multiplicar una matriz por un escalar
    def x(n)
      	resultado = Matriz.new(@matriz)
	for i in 0...@f do
		for j in 0...@c do
			resultado.matriz[i][j] =@matriz[i][j] *n
		end
	end
	resultado
    end
         
     #Metodo para comprobar si dos matrices son iguales
     def igual (mat)
       if(@f == mat.f && @c == mat.c)
	 for i in 0...@f
	   for j in 0...@c
	     if(@matriz[i][j] != mat.matriz[i][j])
	       return -1
	     end
	   end
	 end
       end
       return 1
     end
    #Metodo para calcular el determinante de una matriz
    def deter
        det = @matriz[0][0]
        aux = Matriz.new(@matriz)
        for k in 0...@f do
          l = k+1
          for i in l...@c do
            for j in l...@c do
              aux.matriz[i][j] = (aux.matriz[k][k] * aux.matriz[i][j] - aux.matriz[k][j] * aux.matriz[i][k])/ aux.matriz[k][k]
            end
          end
          det = det * aux.matriz[k][k]
        end
        det
     end
     
     #Metodo para calcular la traspuesta de una matriz
     def t
       resultado = Array.new
       for i in 0...@c
	 resultado[i] = Array.new
	 for j in 0...@f
	   resultado[i][j] = matriz[j][i]
	 end
       end
       resultado
     end
     
         # Metodo para convertir la matriz a string
    def to_s
	    aux = ""
	    @f.times do |i|
		    @c.times do |j|
			    aux << "#{@matriz[i][j]}\t"
		    end
		    aux << "\n"
	    end
	    aux
    end
end
