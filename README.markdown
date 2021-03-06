#Insight

Provides a dashboard that collates information from multiple deployed web application nodes into a single
view.  Insight relies on web applications exposing their configuration properties as a resource, which provides
status information as JSON.

###Example

A request to http://mywebapp:8080/internal/status.json

could respond with a collection of properties:

  {
      "application-version" : "1.0.3",
      "git-commit" : "c7b43bdb9b92a763c8b8",
      "username" :  "user",
      "last-deployed": "16th Feb, 10:45am"
  }
  

##Configuration

Insight is configured as follows:

    {
        "environments": {
            "Staging": {
                "urls":["http://localhost:8081/status.json", "http://localhost:8081/status.json"]
            },
            "Showcase": {
                "urls":["http://localhost:8081/status.json", "http://localhost:8081/status.json"]
            },
            "Prod": {
                "urls":["http://localhost:8081/status.json", "http://localhost:8081/status.json"]
            }
        }
    }

## Example Dashboard

![Insight Dashboard](http://www.ryangreenhall.com/wp-content/uploads/2011/08/insight.png "insight dashboard")


## Getting Started

### Dependencies

The only dependency for using Insight is nodejs which can be downloaded [here](http://nodejs.org/#download)

### Installation
    1. npm install -g insight-dashboard
    2. insight-dashboard --port 3000 --configPath /full/path/to/config.json 
    3. Insight will be running on http://localhost:3000






