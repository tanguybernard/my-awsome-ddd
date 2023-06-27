# Clean architecture

## Introduction

## Apllication


Le usecase implémente une intérface qui fournit un objet InputValues et si il y a un retour un OuputValues.

    public interface UseCase<IntputValues, OutputValues> {
        public OutputValues execute(IntputValues values);
    }
    
    public class CreateUserUseCase implements UseCase<UserDtoInput, UserId> {
    
        public OutputValues execute(IntputValues values){
            //do something
            return UserId(id);
        }
    
    }

## Example

https://github.com/eliostvs/clean-architecture-delivery-example


