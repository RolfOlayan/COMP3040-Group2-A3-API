# General Description of API

## API Description
**How's my prof** is a free online querying tool for professors at the University of Manitoba. Our purpose is to provide information on your past, present, and future instructors using analytics such as faculty, and popularity. We gather our data from the popular **Rate my Professors** as well as the University of Manitoba itself.
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
