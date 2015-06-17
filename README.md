# nativeiosdevelopmenttalk

/

### Objective-C
Person *matt = [[Person alloc] initWithName:@"Matt Galloway"];
[matt sayHello];


### Swift
var matt = Person(name:"Matt Galloway")
matt.sayHello()



String Concatenation


### Objective-C

Person *person = ...;

NSMutableString *description = [[NSMutableString alloc] init];
[description appendFormat:@"%@ is %i years old.", person.name, person.age];
if (person.employer) {
  [description appendFormat:@" They work for %@.", person.employer];
} else {
  [description appendString:@" They are unemployed."];
}


### Swift

var description = ""
description += "\(person.name) is \(person.age) years old."
if person.employer {
    description += " They work for \(person.employer)."
} else {
    description += " They are unemployed."
}






Switch Statements

### Objective-C

if ([person.name isEqualToString:@"Matt Galloway"]) {
  NSLog(@"Author of an interesting Swift article");
} else if ([person.name isEqualToString:@"Ray Wenderlich"]) {
  NSLog(@"Has a great website");
} else if ([person.name isEqualToString:@"Tim Cook"]) {
  NSLog(@"CEO of Apple Inc.");
} else {
  NSLog(@"Someone else);
}


###Swift

switch person.name {
  case "Matt Galloway":
    println("Author of an interesting Swift article")
  case "Ray Wenderlich":
    println("Has a great website")
  case "Tim Cook":
    println("CEO of Apple Inc.")
  default:
    println("Someone else")
}

Pros:
- increased performance over Objective-C
- syntax is more concise and friendly, which decreases length of code and development time

Cons:
- Still a bit buggy after late 2014 release
- New languages means the number of Swift developers is limited
