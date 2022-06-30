Python - Async Comprehension
=

Asynchronous comprehensions are only allowed inside an async def function. Of course, you cannot put Python's await in a comprehension either as that keyword is to be used only inside of an async def function's body. Just for fun, I tried defining an async def function to see if I could make my idea work:


              import asyncio

             async def test(): 
             return [i async for i in range(100) if i % 2]
             loop = asyncio.get_event_loop()
             loop.run_until_complete(test())

Wrapping Up
=

Creating an asynchronous list comprehension is quite a bit different than creating a regular list comprehension. As you can see, it takes a lot more code to make it work. Other than adding the ability to do more asynchronously out of the box, the new asynchronous generator is actually supposed tobe 2x faster than an equivalent implemented as an asynchronous iterator according to PEP 525. While I currently don't have a use case for this new functionality, it is really neat to see what I cando now and I'll be filing these new concepts away for some future application.

