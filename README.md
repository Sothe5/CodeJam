# CodeJam
Some exercise from the CodeJam organized by google

public abstract class ComponentBase{
    public abstract void Operation();
}


public class ConcreteComponent extends ComponentBase{
    @Override
    public void Operation(){
        System.out.println("Component Operation");
    }
}


public abstract class DecoratorBase extends ComponentBase{
    private ComponentBase component;

    public DecoratorBase(ComponentBase component){
        this.component = component;
    }
    @Override
    public void Operation(){
      component.Operation();
    }
}


public class ConcreteDecorator extends DecoratorBase{
    public ConcreteDecorator(ComponentBase component){
      super(component);
    }
    @Override
    public void Operation(){
        super.Operation();
        System.out.println("(modified)");
    }
}
