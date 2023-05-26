# Random Wrapper Interface

| Version | URI                                                                                     | WRAP Version |
|-|-----------------------------------------------------------------------------------------|-|
| 1.0.0 | [`wrap://ens/wraps.eth:random@1.0.0`](https://wrappers.io/v/ens/wraps.eth:random@1.0.0) | 0.1 |

## Interface
```graphql
type Module {
    # get a random Int, bounded by [min, max)
    nextInt(min: Int, max: Int): Int!

    # get a random UInt, bounded by [min, max)
    nextUInt(min: UInt, max: UInt): UInt!

    # get a random Float, bounded by [min, max)
    nextFloat(min: Int, max: Int): BigNumber!

    # get a random Boolean
    nextBoolean: Boolean!

    # get a random byte sequence of the given length
    nextBytes(length: Int!): Bytes!

    # get a random string of the given length
    nextString(length: Int!): String!

    # get a list of random integers with the given length, bounded by [min, max)
    nextInts(length: Int, min: Int, max: Int): [Int!]!

    # an array of randomly sorted integers
    shuffle(length: Int): [Int!]!

    # set the seed of the random number generator for replicable results
    seed(seed: Int!): Boolean!
}
```

## Usage
```graphql
#import * from "ens/wraps.eth:random@1.0.0"
```

And implement the interface methods within your programming language of choice.

## Source Code
[Link](https://github.com/polywrap/std/random)

## Known Implementations
[Link](https://github.com/polywrap/random/tree/master/implementations)