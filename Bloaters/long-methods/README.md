# Long Methods  
Exactly how it sounds. Long methods most likely break the single principle rule of software development. If you feel like you need to write a lengthy comment about what the method does, then it is probably breaking single principle. 

# Ways to fix Long Methods:  
1. use Extract Method tool   
2. If you are unable to use the Extract Method tool because of local variables and parameters.  
    A. Move the small expressions to outside methods and call that method instead.(a.k.a. Replace Temp with Query method).   
    B. If you are having multiple methods have the same parameters, introduce an object with those parameters to reduce the amount of parameters you have (a.k.a. Introduce Parameter Object)  
    C. If you find that you are constantly pulling out values from an object and using them within different methods, instead pass around the object as a whole. (a.k.a. Preserve Whole Object)
3. If 2 doesn't work try: Replace Method with Method Object which Transforms the method into its own class so that local variables come fields of the class.  
4. if conditional loops are to blame for your long method try: decomposing conditional loops. which is seperating your if logic into seperate methods. 
