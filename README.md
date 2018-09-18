# package aula1709;

public class pessoa {
	private String nome;
	private double altura;
	private double peso;
	pessoa (String nome,double altura ,double peso){
		this.nome=nome;
	    this.altura=altura;
		this.peso=peso;
	}
	public double calcImc(){
		return this.peso / (this.altura*this.altura);
	}
		public String classImc (double indice){
		  String c="";
		if (indice <17)
			c= "muito abaixo do peso";
		else if (indice<18.49)
			c= "abaixo do peso";
		else if (indice <24.99)
			c= "peso normal";
		else if (indice < 29.99)
			c= "acima do peso";
		else if (indice<34.99)
			c= "obesidade I";
		else if (indice <39.99)
			c= "obesidade II";
		else if  (indice <40.00)
			c= "obesidade III";				
		return c ;}
		public void relatorio (double i){
			System.out.println ("---------------------------");
			System.out.println ("nome:" +nome);
			System.out.println ("altura:" +altura);
			System.out.println ("imc: " +i);
			System.out.println ("peso:" +classImc(i));
			System.out.println ("---------------------------");
		}}
//////////////////////////////////////////////////////////////////////
package aula1709;

public class teste {
	public static void main(String[] args) {
		pessoa p1 = new pessoa ("Samuel",1.75,60);
		pessoa p2 = new pessoa ("pedro",1.80,90);
		double i;
		i=p1.calcImc();
		i=p2.calcImc();
		
	 	
	
	p1.relatorio(i);
	p2.relatorio(i);
	
	}

}
