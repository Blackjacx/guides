# Interesting Features

## Swift

## [5.6](https://www.hackingwithswift.com/articles/247/whats-new-in-swift-5-6)

## [5.5](https://www.hackingwithswift.com/articles/233/whats-new-in-swift-5-5)
- **Async/Await:** can replace many completion handlers! Especially nested asynchronere function calls.
- **AsyncSequence Protocol:** very useful to e.g. load several objects from a backend and process them as they come in. Reverse geocoding of Locations, processing of locations, etc.
- **Codable synthesis for enums with associated values:** very complex JSON structures are creatable in a simple way
- **Tasks:** as a replacement for operations. Might be easier to handle. Plays perfectly with asynch/await
- **Extend property wrappers to function and closure parameters**
- [NotificationCenter](https://developer.apple.com/documentation/foundation/notificationcenter) includes a new [AsyncSequence API](https://developer.apple.com/documentation/swift/asyncsequence) for receiving notifications using async/await. (74401384)
- A new Swift value type [AttributedString](https://developer.apple.com/documentation/foundation/attributedstring) is now available with the same character-counting behavior as Swift string. It is fully localizable, and also includes support for Markdown, Codable, strongly typed attributes, and more. (27227292)

## [5.4](https://www.hackingwithswift.com/articles/228/whats-new-in-swift-5-4)
- **Improved implicit member syntax** (UIColor.red.cgcolor > .red.cgcolor)
- **Result builders** (can probably be used to auto-chain Operations 🎉)
- **Swift Package Manager caches package dependencies** ([Swift Packages](https://stackoverflow.com/questions/66143815/xcode-12-5-spm-dependency-cache-location))
- Property wrappers are now supported for local variables
- Local functions now support overloading
- 
## [5.3](https://www.hackingwithswift.com/articles/218/whats-new-in-swift-5-3)
- **Swift Package Manager gains binary dependencies, resources, and more**
- **Type-Based Program Entry Points (@main)**
- **multi trailing closures**
- **synthesized comparable for enum types**
- **enum cases as protocol witness**
- increased availability of self in closures
- Multi-pattern catch clauses

## [5.0](https://www.hackingwithswift.com/articles/126/whats-new-in-swift-5-0)

## Alamofire
https://github.com/Alamofire/Alamofire/blob/master/Documentation/Alamofire%205.0%20Migration%20Guide.md#alamofire-50-migration-guide
- **Decodable Responses:** responseDecodable and the DecodableResponseSerializer now provide built-in support for parsing Decodable types from network responses using any DataDecoder type.
- **Encodable Parameters:** Alamofire now supports and prefers Encodable types as parameters using the ParameterEncoder protocol, allowing fully type-safe representation of request parameters.
- **EventMonitor Protocol:** EventMonitors allow access to Alamofire’s internal events, making it far easier to observe specific actions through a request’s lifetime. This makes logging requests very easy.
- **CachedResponseHandler and RedirectHandler Protocols:** Easy access and control over response caching and redirect behaviors, on both a Session and Request basis.
- **HTTPHeaders Type:** Type safe access to common HTTP headers, with extensions to URLRequest, HTTPURLResponse, and URLSessionConfiguration to allow setting the headers of those types using Alamofire’s new type.
- **RetryPolicy:** A RequestRetrier with automatic support for retrying requests which failed due to a network or other system error, with customizable exponential backoff, retry limits, and other parameters.
- **Serializers** updated with more configuration options, including allowed **empty response** methods and codes, as well as the **DataPreprocessor** protocol, to prepare the received Data for serialization (**get rid of the DataWrapper?!**).