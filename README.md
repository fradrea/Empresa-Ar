programa {
	
  funcao inicio() {
	    
	    calcValor()
	    
	}
	
	funcao calcValor(){
	    
	    cadeia empresaNome
		inteiro servicoValor, arQuantidade, descontoPorcentagem, aparelhos_Min, resultado
		caracter continuar = 'S'
	    
	    
	    faca{
	        
	        escreva("Informe o nome da empresa: \n")
	        leia(empresaNome)
	        
	        enquanto(empresaNome == ""){
		        escreva("Por favor informe o nome da empresa: \n")
		        leia(empresaNome)
		    }
		    
		    escreva("Informe o valor do serviço por aparelho: \n")
		    leia(servicoValor)
		    
		    enquanto(servicoValor <= 0){
		        escreva("Por favor informe o valor do serviço por aparelho corretamente: \n")
		        leia(servicoValor)
		    }
		    
		    escreva("Infome o número de aparelhos: \n")
		    leia(arQuantidade)
		    
		    enquanto(arQuantidade <= 0){
		        escreva("Por favor informe número de aparelhos corretamente: \n")
		        leia(arQuantidade)
		    }
		    
		    escreva("Infome a porcentagem do desconto: \n")
		    leia(descontoPorcentagem)
		    
		    enquanto(descontoPorcentagem < 0 ou descontoPorcentagem > 100){
		        escreva("Por favor informe a porcentagem do desconto de 1 a 100: \n")
		        leia(descontoPorcentagem)
		    }
		    
		    escreva("Infome o mínimo de aparelhos para conseguir desconto: \n")
		    leia(aparelhos_Min)
		    
		    enquanto(aparelhos_Min < 0){
		        escreva("Por favor informe número de aparelhos corretamente: \n")
		        leia(aparelhos_Min)
		    }
		    
		    
		    se(arQuantidade >= aparelhos_Min){
    	        se(descontoPorcentagem > 0 e descontoPorcentagem <= 100){
        	        resultado = (servicoValor * arQuantidade) - (servicoValor * arQuantidade * descontoPorcentagem / 100)
        	        escreva("O serviço de " + empresaNome + " custará R$ " + resultado + "\n")
        	        
        	    }senao se(descontoPorcentagem == 0){
        	        resultado = servicoValor * arQuantidade
        	        escreva("O serviço de " + empresaNome + " custará R$ " + resultado + "\n")
        	    }
        	}senao{
        	    resultado = servicoValor * arQuantidade
            	escreva("O serviço de " + empresaNome + " custará R$ " + resultado + "\n")
        	}
		    
		    escreva("Deseja informar novos dados? (S/N)\n")
		    leia(continuar)
		    
	    }enquanto(continuar == 'S')
	    
	}
	
}
