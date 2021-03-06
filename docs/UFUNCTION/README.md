UFUNCTION - Epic Wiki             

UFUNCTION
=========

From Epic Wiki

Jump to: [navigation](#mw-navigation), [search](#p-search)

Contents
--------

*   [1 Description](#Description)
*   [2 Valid Keywords](#Valid_Keywords)
    *   [2.1 BlueprintImplementableEvent](#BlueprintImplementableEvent)
    *   [2.2 BlueprintNativeEvent](#BlueprintNativeEvent)
    *   [2.3 SealedEvent](#SealedEvent)
    *   [2.4 Exec](#Exec)
    *   [2.5 Server](#Server)
    *   [2.6 Client](#Client)
    *   [2.7 NetMulticast](#NetMulticast)
    *   [2.8 Reliable](#Reliable)
    *   [2.9 Unreliable](#Unreliable)
    *   [2.10 BlueprintPure](#BlueprintPure)
    *   [2.11 BlueprintCallable](#BlueprintCallable)
    *   [2.12 BlueprintAuthorityOnly](#BlueprintAuthorityOnly)
    *   [2.13 BlueprintCosmetic](#BlueprintCosmetic)
    *   [2.14 CustomThunk](#CustomThunk)
    *   [2.15 Category](#Category)
    *   [2.16 WithValidation](#WithValidation)
    *   [2.17 ServiceRequest](#ServiceRequest)
    *   [2.18 ServiceResponse](#ServiceResponse)
*   [3 Related](#Related)

Description
===========

Valid Keywords
==============

_These Keywords are also valid for UDELEGATE._

##### BlueprintImplementableEvent

This function is designed to be overridden by a blueprint. Do not provide a body for this function; the autogenerated code will include a thunk that calls ProcessEvent to execute the overridden body.

##### BlueprintNativeEvent

This function is designed to be overridden by a blueprint, but also has a native implementation. Provide a body named \[FunctionName\]\_Implementation instead of \[FunctionName\]; the autogenerated code will include a thunk that calls the implementation method when necessary.

##### SealedEvent

This function is sealed and cannot be overridden in subclasses. It is only a valid keyword for events; declare other methods as static or FINAL to indicate that they are sealed.

##### Exec

This function is executable from the command line.

##### Server

This function is replicated, and executed on servers. Provide a body named \[FunctionName\]\_Implementation instead of \[FunctionName\]; the autogenerated code will include a thunk that calls the implementation method when necessary.

##### Client

This function is replicated, and executed on clients. Provide a body named \[FunctionName\]\_Implementation instead of \[FunctionName\]; the autogenerated code will include a thunk that calls the implementation method when necessary.

##### NetMulticast

This function is both executed locally on the server and replicated to all clients, regardless of the Actor's NetOwner

##### Reliable

Replication of calls to this function should be done on a reliable channel. Only valid when used in conjunction with Client or Server

##### Unreliable

Replication of calls to this function can be done on an unreliable channel. Only valid when used in conjunction with Client or Server

##### BlueprintPure

This function fulfills a contract of producing no side effects, and additionally implies BlueprintCallable.

##### BlueprintCallable

This function can be called from blueprint code and should be exposed to the user of blueprint editing tools.

##### BlueprintAuthorityOnly

This function will not execute from blueprint code if running on something without network authority

##### BlueprintCosmetic

This function is cosmetic and will not run on dedicated servers

##### CustomThunk

The UnrealHeaderTool code generator will not produce a execFoo thunk for this function; it is up to the user to provide one.

##### Category

Specifies the category of the function when displayed in blueprint editing tools. Usage: Category=CategoryName or Category="MajorCategory,SubCategory"

##### WithValidation

This function must supply a \_Validate implementation

##### ServiceRequest

This function is RPC service request

##### ServiceResponse

This function is RPC service response

Related
=======

[UCLASS](/index.php?title=UCLASS&action=edit&redlink=1 "UCLASS (page does not exist)"), [UPROPERTY](/UPROPERTY "UPROPERTY"), [USTRUCT](/index.php?title=USTRUCT&action=edit&redlink=1 "USTRUCT (page does not exist)"), [UMETA](/index.php?title=UMETA&action=edit&redlink=1 "UMETA (page does not exist)"), [UPARAM](/index.php?title=UPARAM&action=edit&redlink=1 "UPARAM (page does not exist)"), [UENUM](/index.php?title=UENUM&action=edit&redlink=1 "UENUM (page does not exist)"), [UDELEGATE](/index.php?title=UDELEGATE&action=edit&redlink=1 "UDELEGATE (page does not exist)")

Retrieved from "[https://wiki.unrealengine.com/index.php?title=UFUNCTION&oldid=2430](https://wiki.unrealengine.com/index.php?title=UFUNCTION&oldid=2430)"