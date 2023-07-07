# Clean architecture

## Introduction

## Application

### Variant 1

Le usecase implémente une interface qui fournit un objet InputValues et si il y a un retour un OuputValues.

    public interface UseCase<IntputValues, OutputValues> {
        public OutputValues execute(IntputValues values);
    }
    
    public class CreateUserUseCase implements UseCase<UserDtoInput, UserId> {
    
        public OutputValues execute(IntputValues values){
            //do something
            return UserId(id);
        }
    
    }


### Variant 2 (better)


    // Use Case Output Port
    interface Presenter
    {
        public void accept(Aggregate aggregate);
        public Dto getPresentedState();
        
    }


    public class CreateUserUseCase  {
    
        private Repository repository;
        private Presenter presenter;
    
        public CreateUserUseCase(Repository repository, Presenter presenter){
            this.repository = repository;
            this.presenter = presenter;
        }
    
        public void execute(User user){ // or dto ?
    
            User userSaved = repository.save(user);
            presenter.accept(userSaved);
    
    
            //IMPORTANT: execute method return nothing, we use presenter
            
        }
        
    }


    class Controller
    {
        public void ExecuteUseCase(Data data)
        {
            Request request = ...
            Repository repository = new PgRepository;
            Presenter presenter = new JsonPresenter();
            UseCase useCase = new UseCase(repository, presenter);
            useCase.execute(request);
            return presenter.getPresentedState();
        }
    }


## Example

https://github.com/eliostvs/clean-architecture-delivery-example


