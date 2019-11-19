### Mediator Pattern - Inter component Communication

- Used for communicating between components 
- Each child component can use reference to parent to broadcast a message
- Each child listen to the message and decide to take an action if required
- NOTE :The message is also broadcasted to the source component, so it must ignore it to avoid loop.
- Outline 
```
class ComponentContainer {
	public void send(String message){
		for(Component component : componentList){
			component.receive(message);
		}
	}

	private List<Component> componentList;

}

interface Component {
	public void receive(String message);
}
```



