- 👋 Hi, I’m @amnanoorulain
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
amnanoorulain/amnanoorulain is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
     Video Url- https://youtu.be/uD8iEX7VoPw

1. Go To Shared Components >> Templates >> Search by typing Cards
	Copy Report Card- Name- Product Card UI Design
	Open your copied Templates Product Card UI Design

	Row Templates1 >> Paste the following code

	<li class="containers #CONTAINER_CLASS#">
        <div class="card">
                <div style="width: 200px; margin: 5px; box-shadow: 5px 5px 15px rgba(0,0,0,0.9); transition: 0.5s ease; cursor: pointer; border-radius: 30px; margin: 15px;">
                    <div style="width: 100%; height: 150px; justify-content: center; align-items: center; background: #fa782e; background: -moz-linear-gradient(-45deg, #fa782e 8%, #c82930 83%); background: -webkit-linear-gradient(-45deg, #fa782e 8%, #c82930 83%); background: linear-gradient(135deg, #fa782e 8%, #c82930 83%); filter: progid: DXImageTransform.Microsoft.gradient( startColorstr=#fa782e, endColorstr=#c82930, GradientType=1); border-radius: 25px 25px 0 0;">
                        #CARD_IMAGE#
                    </div>

                <div style=" width: 100%; background: #fff; border-radius: 0 0 25px 25px;">

                        <div class="product-desc">
                            <span style="padding: 0px 0px 10px 10px; display: inline-block; font-size: 16px; letter-spacing: 1px; text-align: left; margin-top: 58px;">
                                <b>#CARD_TEXT#</b>
                            <span style="padding: 0px 5px; font-size: 11px; text-align: center; display: block;">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star grey"></i>
                            </span>
                        </div>
                            <div style="width: 100%; padding: 0px 0px 15px 10px; text-align: center;">
                                <span class="product-size">
                                    <ul class="ul-size">
                                        <li><a href="#" style="background: #f35e3d; color: #fff;">S</a></li>
                                        <li><a href="#" style="background: #f35e3d; color: #fff;">M</a></li>
                                        <li><a href="#" style="background: #f35e3d; color: #fff;">L</a></li>
                                        <li><a href="#" style="background: #f35e3d; color: #fff;">XL</a></li>
                                        <li><a href="#" style="background: #f35e3d; color: #fff;">XXL</a></li>
                                    </ul>
                                </span>
                            </div>

                            <div style="display: inline-block; padding: 10px 0px 8px 10px;"><span style="text-align: left; font-size: 15px; padding: 10px 10px 10px 10px;">TK-<b>#PRICE#</b></span>
                                <span style="text-align: left; font-size: 12px; text-decoration: line-through;"><b>#SELLPRICE#</b></span>
                                <span style="font-size: 12px;"<b>#DISPRICE#</b></span>
                            </div>

                            <div style="padding: 5px 0px 15px 15px;"> 
                                <a href="#LINK#"><div <span style="background-color: #f44336; color: white; width: 90%; font-size: 1.8rem; padding: 0.6rem; font-weight: 600; border-radius: 20px 20px; text-align: center; fa-shopping-cart: before {;content: "\f07a"; margin-top: 8px;"> <i class="fa fa-shopping-cart" aria-hidden="true"></i> Add Cart</div></a>
                            </div>           


        </div>
    </div>
</div>
</li>
================================================================

	All other Templates will be blank
	Click on Apply Change

2. Create a New Blank page. Name- Product Card UI Design

3. Create a Classic Report. Name-Product Card Report

	SQL Query- 	
		SELECT a.PRODUCT_ID,
       DBMS_LOB.getlength (a.PRODUCT_IMAGE) AS CARD_IMAGE,
       a.PRODUCT_DESCRIPTION AS DESCRIPTION,
       a.PRODUCT_NAME CARD_TEXT,
       a.PRODUCT_CODE,
       (SELECT p.ORIGINAL_PRICE
          FROM PRODUCT_PRICE p
         WHERE a.PRODUCT_ID = p.PRODUCT_ID)
          AS PRICE,
       (SELECT p.SELLING_PRICE
          FROM PRODUCT_PRICE p
         WHERE a.PRODUCT_ID = p.PRODUCT_ID)
          AS SELLPRICE,
       (SELECT p.DISCOUNT
          FROM PRODUCT_PRICE p
         WHERE a.PRODUCT_ID = p.PRODUCT_ID)
          AS DISPRICE
  FROM PRODUCT a
=====================================================================================

4. Go To Report Attributes >> Template >> Product Card UI Design

5. Inline Css >> 

	.t-Cards {
    /* list-style: none; */
    /* padding: 0; 
    margin: -8px;*/
    /* overflow: hidden; */
    flex-wrap: wrap;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    align-content: center;
    align-self: center;
    text-align: center;
    transition: 0.5s ease; 
    cursor: pointer; 
}

.card {
     width: 200px;
    margin: 5px;
     /*   box-shadow: 5px 5px 15px rgba(0,0,0,0.9);
     border-radius: 30px; */
    transition: 0.5s ease;
    cursor: pointer;
    
    margin: 15px;
}

.card:hover {
    transform: scale(1.03);
}

img {
    width: 100%;
    height: 200px;
    padding: 10px 10px 10px 10px;
    border-radius: 32px 32px 0 0;
/*    margin-top: 10px;  */
}

.product-size h4 {
    font-size: 13px;
    padding: 0px 10px;  
    margin-top: 3px;
    /* padding-bottom: 3px; */
    /* text-transform: uppercase; */
    text-align: left;
    /* margin-left: 21px; */
}

.ul-size {
    margin: auto;
    padding: 0px 0px 0px 10px;
}

.ul-size li {
  list-style: none;
  float: left;
  margin-right: 5px;
  text-align: left;
}


.ul-size li a {
    display: inline-block;
    /* text-decoration: none; */
    font-size: 10px;
    font-weight: 600;
    width: 23px;
    height: 23px;
    border-radius: 100%;
    text-align: center;
    line-height: 25px;
    color: #000;
}

