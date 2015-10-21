       OOP PRINCIPALS
ABSTRACTION Abstraction means working with something we know how to how to use without knowing how it work internily. E.g we don't need to know inner working of a TV,in order to use it.just we need a remote with small set of buttons (interface of the remote) and we will be able to watch the tv.it is same in objects of the oop.Abstraction is that we can do every day. for example ,in hardware configuration, this is called
'Abstraction' data storage device which can be hard disk, USB memory stick or CD-ROM drive.

      Abstraction is one of the most important concepts in programming and OOP. It allows us to write code,     which works with abstract data structures (like dictionaries, lists, arrays and others). We can work with an abstract data type by using its interface without concerning ourselves with its implementation. For instance, we can save to a file all elements from a list without bothering if it is implemented with an array, a linked list, etc. The code remains unchanged, when we work with other data types. We can even write new data types (we will discuss this later) and make them work with our program without changing it.                                                                                                                                                                                                                           
public class AbstractionExample { static void Main() { Lion lion = new Lion(true, 150); Felidae bigCat1 = lion;

    AfricanLion africanLion = new AfricanLion(true, 80);
    Felidae bigCat2 = africanLion;
}
} Encapsulation Encapsulation means information hiding. An object has to provide its users only with the essential information for manipulation, without the internal details. Everything else is hidden internally under the cover. She does not know about the inner workings of Laptop, because she doesn’t need to, and if she does, she might make a mess. Therefore parts of the properties and methods remain hidden to her. The person writing the class has to decide what should be hidden and what not. When we program, we must define as private every method or field which other classes should not be able to access. Eg. public class Lion : Felidae, Reproducible { // …

private Paw frontLeft;
private Paw frontRight;
private Paw bottomLeft;
private Paw bottomRight;

private void MovePaw(Paw paw) {
    // …
}

public override void Walk()
{
    this.MovePaw(frontLeft);
    this.MovePaw(frontRight);
    this.MovePaw(bottomLeft);
    this.MovePaw(bottomRight);
}

// …
} Polymorphism. The next fundamental principle of Object-Oriented Programming is "Polymorphism". Polymorphism allows treating objects of a derived class as objects of its base class. For example, big cats (base class) catch their prey (a method) in different ways. A Lion (derived class) sneaks on it, while a Cheetah (another derived class) simply outruns it. Polymorphism allows us to treat a cat of random size just like a big cat and command it "catch your prey", regardless of its exact size. Polymorphism can bear strong resemblance to abstraction, but it is mostly related to overriding methods in derived classes, in order to change their original behavior inherited from the base class. Abstraction is associated with creating an interface of a component or functionality (defining a role). We are going to explain method overriding shortly. Inheritance Inheritance is a fundamental principle of object-oriented programming. It allows a class to "inherit" (behavior or characteristics) of another, more general class. For example, a lion belongs to the biological family of cats (Felidae). All cats that have four paws, are predators and hunt their prey. This functionality can be coded once in the Felidae class and all its predators can reuse it – Tiger, Puma, Bobcat, etc. Inheritance is described as is-kind-of relationship, e.g. Tiger is kind of Animal. E.g
///

Felidae is latin for "cats"
public class Felidae { private bool male;
// This constructor calls another constructor
public Felidae() : this(true)
{}

// This is the constructor that is inherited
public Felidae(bool male)
{
    this.male = male;
}

public bool Male
{
    get { return male; }
    set { this.male = value; }
}
}
