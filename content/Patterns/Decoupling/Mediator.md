#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=78]]
# Intent
Define an object that encapsulates how a set of objects interact. Mediator promotes loose coupling by keeping objects from referring to each other explicitly, and it lets you vary their interaction independently.

# Structure of Mediator
![[Pasted image 20260208192706.png]]
# Example of Mediator
- Often there are dependencies between the widgets(buttons, menus, entry fields, etc.) in a dialog box. For example, a button gets disabled when a certain entry field is empty.
- Different dialog boxes will have  different dependencies between widgets.
- Customizing them individually in subclasses will be tedious, since many classes are involved.
$==>$ encapsulate collective behavior in a seperate mediator object
![[Pasted image 20260208193320.png]]

# Applicability
- when a set of objects communicate in well-defiled but complex ways. The resulting interdependencies are unstructured and difficult to understand
- When a behavior that's distributed between several classes should be customizable without a lot of subclassing.
- When a behavior that's distributed between several classes should be customizable without a lot of subclassing.

