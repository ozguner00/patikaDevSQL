Aşağıdaki sorgu senaryolarını örnek veri tabanı üzerinden gerçekleştiriniz.

1.City tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.  
2.Customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.  
3.Customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.  

1.**SELECT** city,country **FROM** city  
**LEFT JOIN** country **ON** city.country_id = country.country_id  

2.**SELECT** payment.payment_id,customer.first_name, customer.last_name **FROM** customer  
**RIGHT JOIN** payment **ON** customer.customer_id = payment.customer_id

3.**SELECT** rental.rental_id, customer.first_name, customer.last_name **FROM** customer  
**FULL JOIN** rental **ON** rental.rental_id = customer.customer_id

<details> <summary>3. Mysql </summary>
SELECT rental.rental_id, customer.first_name, customer.last_name FROM customer   
  
LEFT JOIN rental ON rental.rental_id = customer.customer_id     
UNION    
SELECT rental.rental_id, customer.first_name, customer.last_name FROM customer    
RIGHT JOIN rental ON rental.rental_id = customer.customer_id</details>   
