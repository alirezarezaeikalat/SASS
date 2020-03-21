1. To use .scss files we have to compile them
to css files, we can do this in two ways:

    a. using cli options for sass
    b. usign different softwares

we make .scss files and the app translate it to
.css files

2. use prepros app for the translation

3. we can use variables in sass like this:

  /// variables
  $sectionHeading : 24px;
  
  h1 {
    font-size: $sectionHeading;
  }

4. Using nested styles:
    we can use nested styles in sass:

    #main-nav{
      ul{

      }
    }
  this is like: #main-nav ul{} 

5. using mixins to avoid code duplication:
    (using mixin is just like we select
     a element then we have to include it)

    @mixin mixinName{

    }

    .lead-banner{
      @include mixinName;
    }

6. We can have multiple sass files and import in
  one file in order, we have to un tick 
  auto compile in prepos app:

  @import "mixins";
  @import "variables";

7. To use pseudo classes in sass, we can add
pseudo class in the selector itself wiht &:

ul{
  color: white;
  a{
    &:hover{
      background-color: #333;
    }
  }
}

8. We can use math operators in sass:

  width: (100% / 6);

9. We can pass arguments to mixins:

  @mixin grid($cols, $margin){
    width: 100% / $cols;
    margin-right: $margin;
    &:nth-child(#{$cols}n){
      margin-right: 0;
    } 
  }
to include it:
  
  @include grid(6, 4%);
