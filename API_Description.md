# General Description of API

## API Description

## Endpoints & Parameters

## Resources
- This API has a faculty resource which contains faculty and rating attributes. The faculty attribute includes the name of the faculty of the University of Manitoba, and the rating incorporates the number of rates for each faculty.

```
class facutlysource 
    
    attributes :faculty, :rating
    
    # faculty setter 
    def faculty = (new_faculty)
        @model.faculty = new_faculty
    end
    
    # rating_num setterr
    def rating = (new_rating)
        @model.rating = new_rating
    end
    
    # faculty getter
    def faculty 
        @model.faculty.to_s
    end
    
    # rating getter
    def rating
        @model.rating.to_i
    end
end
```

## Sample Requests & Sample Responses
