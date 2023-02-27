# narayan-sdk
Python SDK that makes the `Lord Of the Rings` API accessible to other developers. The SDK covers only the movie endpoints:  
```
/movie
/movie/{id}
/movie/{id}/quote
```
**Please Note:** Details of the design and how to run it locally or use the package in your client code can be found in `DESIGN.md`

The name of the package is `lotr-sdk-iyerland` and published to Python Package Index (PyPi).

## Assumptions
Python3 & Pip3 are already installed on the target machine where this 
repo will be cloned and tested.

## How to unit test the code
After checking out the code (from github) and while in project folder, run:
```
python3 -m unittest
```

## How to test/run the code
Detailed in `DESIGN.md`.

## Self-Evaluation Survey

0. Why did I use `Python`?
A. My strong point is Scala, but I chose to solve it in `Python` as the libraries
are straight forward and simple, and I did not wanted to get bogged down in a complex
solution using Monads and other functional effect solutions. 

1. Have you manually tested the SDK?
A. Yes, it is detailed in the `DESIGN.md` doc. I tested the SDK in the python shell.

2. Did you add a test suite? How will we use it?
A. Yes. While it is not comprehensive, managed to add a few test cases. It is explained above.

3. Did you use any third party library? Why did you use it? What are the trade-offs?
A. I used `urllib3` which was pretty straightforward for the job at hand. But mainly it addressed the following concerns (not that I planned to use all the features):
- Thread safety
- Connection pooling
- Client-side SSL/TLS verification
- File uploads with multipart encoding
- Helpers for retrying requests and dealing with HTTP redirects
- Support for gzip and deflate encoding
- Proxy support for HTTP and SOCKS
It is a 3rd part library as opposed to being part of the standard library, so it needs to be installed separately through `pip3`.

4. Do you feel this SDK makes it easier to interact with the API?
A. Yes, definitely, it completely abstracts the API, and can make it easier to use, in fact, if needed, can also be customized, if a high-paying customer demands it.

5. If you had more time, what else would you add?
A. Currently, it is very basic, I did it in a language, which is not my strong point. But I would re-implement in a statically & strongly typed language, like say `Rust` which is performant and a minimalist language (comparitively). I would define separate classes for each resource like `Movie`, `Character`, `Quote` and have functions associated with them. Ensure proper error handling and messaging and retries which would all be configurable. These all would be part of different packages like `domain`, `client`, `common` and neatly designed.

6. What would you change in your current SDK solution?
A. See answer to 5.

7. On a scale of 1 to 10, how would you rate this SDK? (higher is better).
A. I would rate it as a 7 as it works, and has a minimal test suite and does what its supposed to do, in a language, which is not my strong point and has error handling and retries, albeit very basic.

8. Anything else we should keep in mind when we evaluate the project?
A. We are all creatures of habbit and tend to remember and fluent at what we've been working on recently and that SDK was one of the artifacts that I have least worked on in my career. So please judge accordingly. I was more interested in getting a MVP out of the door ASAP. So time was something I was very conscientious about!
