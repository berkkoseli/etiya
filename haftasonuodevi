
--1. Kargo şirketlerine toplam kaç para ödendiğini hesaplayınız.

select sum(shipping_fee) as ÖDENECEK_TUTAR from cargo_companies;


--2. Halihazırda indirimli ve isminde 'b' geçen tüm ürünleri listeleyiniz.
--products tablosunun içersine (at_a_discount) adında boolean değer alan kolon eklenmiştir.
  --at_a_discount = TRUE ise ürün indirimdedir.
   
   
   select * from products as p
   where  (p.at_a_discount is TRUE) AND  (LOWER(p.name) LIKE '%b%')
   
   
3. 3.harfi c olan tüm ürünleri getiriniz.
-- küçük harf c ve büyük harf C dikkate alınmalıdır.

  select * from products as pro
  where pro.name LIKE '__c%' or pro.name LIKE '__c%'
  

4.-Bir kişinin sipariş oluştururken kullanacağı insert komutlarını yazınız (alt tablolar dahil ve siparişte en az 3 ürün olacak şekilde)

insert into 
order_details (order_number,quantity,product_id,order_id,order_total_price)
values
(91,5,(select products.id from products where products.name='etek'),5,100),
(87,10,(select products.id from products where products.unit_price=150.00),1,1500),
(33,10,(select products.id from products where products.stock<=25),2,2000);



