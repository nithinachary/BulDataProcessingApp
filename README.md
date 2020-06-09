# BulDataProcessingApp #
----------------------------

This project aims at having different APIs for multiple files actions like upload, download, get all files etc.

----------------------------------------------------
APIs details with path, sample request and response
----------------------------------------------------

1. Upload File 

      Sample Request          : {URL : http://localhost:3000/bulk/uploadFile, Method : POST, Body : FileName }                           
      Sample response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Uploaded The File","data":""}                       
      Sample error response   : {"code":404,"status":"FAILED","msg":"The specified file does not exist","data":""}                       
      Validation error        : {}
      
2. Upload Multiple File 

      Sample Request          : {URL : http://localhost:3000/bulk/uploadMultipleFile, Method : POST, Body : [FileName1,FileName2] }
      Sample response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Uploaded All The Files","data":""}                   
      Sample error response   : {"code":404,"status":"FAILED","msg":"The specified file does not exist","data":""}                       
      Validation error        : {}
      
3. Download file
  
      Sample Request          : {URL : http://localhost:3000/bulk/getFile?file="", Method : GET, Params : FileName }                     
      Sample response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Downloaded The File","data":""}                     
      Sample error response   : {"code":404,"status":"FAILED","msg":"The specified file does not exist","data":""}                       
      Validation error        : {}
 
 4. List All files
  
      Sample Request          : {URL : http://localhost:3000/bulk/listAllFiles, Method : GET }                                           
      Sample response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Fetched All The File","data":""}                     
      Sample error response   : {"code":404,"status":"FAILED","msg":"No files found","data":""}                                         
      Validation error        : {}
      
 5. Get File Detials
 
      Sample Request          : {URL : http://localhost:3000/bulk/getFileDetails?file=sample, Method : GET, Params : FileName}           
      Sample Response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Fetched The Given File Details","data":""}           
      Sample error response   : {"code":404,"status":"FAILED","msg":"No file found","data":""}                                           
      Validation error        : {}
      
 6. User Login
     
      Sample Request          : {URL : http://localhost:3000/users/login, Method : GET,                                                 
                                                            Body: {"email":"nitin@gmail.com","password":"password"}}                     
      Sample Response         : {"code":200,"status":"SUCCESS","msg":"Successfullly Logged In","data":""}                               
      Sample error response   : {"code":404,"status":"FAILED","msg":"No Such User Found. The email address is not
                                                 associated with any account. Double-check your email address and try again.","data":""}       Sample error response   : {"code":401,"status":"FAILED","msg":"Invalid Email Or Password","data":""}                               
      Sample error response   : {"code":401,"status":"FAILED","msg":"Your account has not been verified","data":""}                     
      Validation error        : {}
      
 7. User Registration
  
      Sample Request          : {URL : http://localhost:3000/users/registerUser, Method : POST,
                                                                               Body: {"email":"nitin@gmail.com","password":"password"}} 
      Sample Success Response : {"code":200,"status":"SUCCESS","msg":"A verification email has been sent to email","data":""}           
      Sample error response   : {"code":401,"status":"FAILED","msg":"The email address you have entered is already registered"
                                                                                          ,"data":"Registratoion Id" }                   
      Validation error        : {}
      
 8. User Verification
  
      Sample Request          : {URL : http://localhost:3000/users/verifyUser, Method : GET, 
                                                         Body: {"email":"nitin@gmail.com","token":"0aace84f8bf5c3393e2505e0541fd9e3"}}   
      Sample Success Response : {"code":200,"status":"SUCCESS","msg":"A verification email has been sent to email","data":""}           
      Sample error response   : {"code":401,"status":"FAILED","msg":"This user has already been verified","data":""}                     
      Sample error response   : {"code":401,"status":"FAILED","msg":"Token expired. Please check with Admin","data":""}                 
      Validation error        : {}
      
 9. User Cart Details
  
      Sample Request          : {URL : http://localhost:3000/users/userCart, Method : POST, 
                                                                         Body: {{"userId":"1","fileName":"achary.txt","quantity":2}}}   
      Sample Success Response : {"code":200,"status":"SUCCESS","msg":"Item added to the cart","data":cart}                               
      Sample error response   : {"code":404,"status":"FAILED","msg":"No Such File Found","data":""}                                     
      Sample error response   : {"code":401,"status":"FAILED","msg":"Quantiy should be greater than 0","data":""}                       
      Sample error response   : {"code":401,"status":"FAILED","msg":"Item already added to cart","data":""}                             
      Validation error        : {}
      
 10. Final Paying Amount/ Final Purchase
  
      Sample Request          : {URL : http://localhost:3000/users/getFinalPaymentDetails?userId=1, Method : GET, Params: userId}       
      Sample Success Response : {"code":200,"status":"SUCCESS","msg":"Item added to the cart","data":"Final Payable Amount = "}         
      Sample error response   : {"code":404,"status":"FAILED","msg":"No User Found","data":""}                                           
      Sample error response   : {"code":404,"status":"FAILED","msg":"No Valid Cart for the given User","data":""}                       
      Validation error        : {}
 
 
    
  
  
