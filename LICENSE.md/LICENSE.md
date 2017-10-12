package haftabes;
import java.util.Scanner;

public class boykilo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		double bmisonucu;
		double poundgirdi, incgirdi;
		double pounddönüstür, incdönüstür;
		final double KİLOGRAMS_PER_POUND = 0.45359237 ;
		final double METERS_PER_INCH = 0.0254 ;
		Scanner input = new Scanner(System.in);
		System.out.println("kilonuzu pound olarak giriniz");
		poundgirdi = input.nextDouble();
		System.out.println("boyunuzu inch olarak giriniz");
		incgirdi = input.nextDouble();
		pounddönüstür = poundgirdi * KİLOGRAMS_PER_POUND ;
		incdönüstür = incgirdi * METERS_PER_INCH ;
		System.out.println("kilonuz " + String.format("%.2f",pounddönüstür)
				+ " boyunuz " +String.format("%.2f",incdönüstür*100) +" cm");
		bmisonucu = pounddönüstür / (incdönüstür * incdönüstür);
		System.out.println("bmi sonucunuz " + bmisonucu);
		if(bmisonucu < 18.5)
			System.out.println("underwight");
		else if (bmisonucu < 25)
			System.out.println("Normal");
		else if (bmisonucu < 30)
			System.out.println("overweight");
		else 
			System.out.println("obez");
	}

}
