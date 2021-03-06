# rack-subdomain

Rack middleware to transparently route requests with a subdomain to a specified path with substitutions. 

## Usage

### Gemfile

``` ruby
gem 'rack-subdomain'
```

### config.ru

``` ruby

# Simple Example

use Rack::Subdomain, "example.com", to: "/users/:subdomain"

# Complex Example
use Rack::Subdomain, "example.com", except: ['', 'www', 'secure'] do
  map 'downloads', to: "/downloads/:subdomain"
  map '*', to: "/users/:subdomain"
end
```

## Contact

Mattt Thompson

- http://github.com/mattt
- http://twitter.com/mattt
- m@mattt.me

## License

rack-subdomain is available under the MIT license. See the LICENSE file for more info.
