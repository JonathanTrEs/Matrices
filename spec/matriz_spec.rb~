require 'Matriz' 
require 'rspec'

describe Matriz do
  
	before :each do
		@m1 = Matriz.new([[1,2],[3,4]])
		@m2 = Matriz.new([[1,1],[1,1]])
		@m3 = Matriz.new([[4,3],[2,1]])
		@m4 = Matriz.new([[1,2,3],[4,5,6]])
		@m5 = Matriz.new([[Fraccion.new(1,2),Fraccion.new(1,2)],[Fraccion.new(1,2),Fraccion.new(1,2)]])
		@m6 = Matriz.new([[Fraccion.new(2,3),Fraccion.new(2,3)],[Fraccion.new(2,3),Fraccion.new(2,3)]])
		@m7 = Fraccion.new(7,6)
		@m8 = Fraccion.new(1,6)
		@m9 = Fraccion.new(2,3)
		@n = 2
	end
		
	describe "Pruebas constructor" do

		it "Debe existir una variable que almacene el numero de filas" do
			@m1.f.should == 2
			@m5.f.should == 2
		end

		it "Debe existir una variable que almacene el numero de columnas" do
			@m1.c.should == 2
			@m5.c.should == 2
		end
		
		it "Se debe invocar al metodo f() para obtener el numero de filas" do
			@m1.respond_to?("f").should be_true
			@m5.respond_to?("f").should be_true
		end
		
		it "Se debe invocar al metodo c() para obtener el numero de columnas" do
			@m1.respond_to?("c").should be_true
			@m5.respond_to?("c").should be_true
		end
	end
  
        describe "Puebas operaciones binarias" do
	  
		it "Se debe sumar dos matrices con + y dar el resultado" do
			(@m1 + @m2).matriz == [[2,3],[4,5]]
			(@m5 + @m6).matriz == [[@m7,@m7],[@m7,@m7]]
		end
		
		it "Se debe restar dos matrices con - y dar el resultado" do
			(@m1 - @m2).matriz == [[0,1],[2,3]]
			(@m6 - @m5).matriz == [[@m8,@m8],[@m8,@m8]]
		end
		
		it "Se debe multiplicar dos matrices con * y dar el resultado" do
			(@m1 * @m3).matriz == [[8,5],[20,13]]
			(@m5 * @m6).matriz == [[@m9,@m9],[@m9,@m9]]
		end
		
		it "Se debe multiplicar una matriz pro un escalar y dar el resultado" do
			@m1.x(@n).matriz == [[2,4],[6,8]]
		end
		
		it "Se debe comparar si dos matrices son iguales" do
			(@m1.igual(@m1)).should == 1
			(@m5.igual(@m6)).should == -1
			(@m5.igual(@m5)).should == 1
		end
	end
     

        describe "Pruebas unarias" do
	  
		it "Se debe calcular el determinante de una matriz" do
			@m1.deter == -2
		end
		
		it "Se debe mostar por la consola la Matrix en forma de string"do
			@m1.to_s.should == "1\t2\t\n3\t4\t\n"
		end

		it "Se debe calcular la traspuesta de una matriz" do
		  @m4.t.should == [[1,4],[2,5],[3,6]]
		end
	end

end
