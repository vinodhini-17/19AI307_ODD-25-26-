# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To write a Java program to implement the Model View Controller (MVC) design pattern for managing product details.

## ALGORITHM :
1. Start the program.
2. Create a Product class as the model with product name and price.
3. Create a ProductView class to display product details.
4. Create a ProductController class to update product details and refresh the view.
5. Create a Product object with initial values.
6. Create the view and controller objects.
7. Display the initial product details.
8. Update the product price using the controller.
9. Refresh and display the updated product details.
10. End the program.
    
## PROGRAM:
 ```
/*
Program to implement MVC design pattern using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ProductManagementSystem 
{

    static class Product 
    {
        private String name;
        private double price;
        private String code;

        public Product(String name, double price, String code) 
        {
            this.name = name;
            this.price = price;
            this.code = code;
        }

        public String getName() 
        {
            return name;
        }

        public double getPrice() 
        {
            return price;
        }

        public String getCode()
        {
            return code;
        }

        public void setPrice(double price) 
        {
            this.price = price;
        }
    }

    static class ProductView 
    {
        public void displayProduct(String name, double price, String code) 
        {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    static class ProductController 
    {
        private Product product;
        private ProductView view;

        public ProductController(Product product, ProductView view) 
        {
            this.product = product;
            this.view = view;
        }

        public void updateView() 
        {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }

        public void updatePrice(double newPrice) 
        {
            product.setPrice(newPrice);
            updateView();
        }
    }

    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();

        double price = sc.nextDouble();

        sc.nextLine();

        String code = sc.nextLine();

        double newPrice = sc.nextDouble();

        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        controller.updateView();

        controller.updatePrice(newPrice);

        sc.close();
    }
}
```

## OUTPUT:
<img width="1295" height="443" alt="image" src="https://github.com/user-attachments/assets/76e7465c-909b-45b5-b0f2-61c1d70b8244" />

## RESULT:
The Java program was executed successfully and the product details were updated and displayed successfully using the MVC design pattern.
