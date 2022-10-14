# Classes

The [class declaration](https://kotlinlang.org/docs/reference/classes.html#classes) consists of the class name, the class header (specifying its type parameters, 
the primary constructor etc.) and the class body, surrounded by curly braces. 
Both the header and the body are optional; if the class has no body, curly braces can be omitted.

```run-kotlin
class Customer( val name: String) {
    fun displayName(){
        println("Name Of The Customer ${name}")
    }
}                                 

class Contact(val id: Int, var email: String,val ph_Number:String){
    fun displayCustomerDetails(){
        println("id of the customer ${id} \nEmail Of The Customer ${email} \nPhone number of the customer ${ph_Number}")
    }
}

fun main() {

    val customer = Customer("XYZ")                   // 3
    customer.displayName()
    val contact = Contact(1, "mary@gmail.com" , "0345678321")
    contact.displayCustomerDetails()
}```

1. Declares a class named `Customer` without any properties or user-defined constructors. A non-parameterized default constructor is created by Kotlin automatically.
2. Declares a class with two properties: immutable `id` and mutable `email`, and a constructor with two parameters `id` and `email`.
3. Creates an instance of the class `Customer` via the default constructor. Note that there is no `new` keyword in Kotlin.
4. Creates an instance of the class `Contact` using the constructor with two arguments.
5. Accesses the property `id`.
6. Updates the value of the property `email`.
