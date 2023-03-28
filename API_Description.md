# General Description of API

## API Description
**How's my prof** is a free online querying tool for professors at the University of Manitoba. Our purpose is to provide information on your past, present, and future instructors using analytics such as faculty, and popularity. We gather our data from the popular **Rate my Professors** as well as the University of Manitoba itself.
## Endpoints & Parameters

## Resources
This API has a professor resource which contains name, faculty, and rating attributes. The name attribute contains the name of the professor. The faculty attribute includes the name of the faculty to which the professor belongs. Finally, the rating incorporates the rates for each professor.

```
class ProfessorResource 
    
    attributes :name, :faculty, :rating
    
    # name setter
    def name = (new_name)
        @model.name = new_name
    end
    
    # faculty setter 
    def faculty = (new_faculty)
        @model.faculty = new_faculty
    end
    
    # rating setter
    def rating = (new_rating)
        @model.rating = new_rating
    end
    
    # name getter
    def name 
        @model.name.to_s
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
