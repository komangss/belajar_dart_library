## Learn Notes :
This dart project is made by 
``dart create --template=package-simple belajar_dart_library``

if you are creating a dart file with ``dart create``
that means you are using template compile-simple

we use template package-simple insteads

## Dart packages :
Dart ecosystem is using package as the software management and this is provided by dart by default. Some of other programming language like PHP or Java is not have a software management system by default. instead they are using third party like Gradle or Maven for Java, and Composer for PHP.
Minimaly we only need pubspec.yaml and lib folder when we create a dart packages, but when we using dart create, the directory structure will be a little bit complex.
Packages can be a library or application.

## Benefit of using packages in Dart :
Standarize how we manage our code and folder in Dart
Handling dependency management is more easy because we dont need to download library that we need manually


## Directory explanation :
- pubspec.yaml is used for dart packages configuration
- Changelog.md is usually for version
- analysis_options.yaml is usually for 'static code analysis'
- /lib/ folder is the place we put our dart code.
- /test/ folder is unit test
- /example/ folder is will be the folder where we use for example when using our main dart code (in /lib/ folder)

## Directory src :
One of dart best practice in dart packages is not exposing code if dont need to.
Practically for that best practice is put the dart code in /**src**/  folder in /lib/ folder.
All code in /src/ folder will not be exposed to external (can accessed by other project) by deafult.
When we need to expose the code for external, we put the code in /lib / folder.
We can use code in the /src/ folder but it is not recommended because code inside the /src/ folder is not guaranteed for decode competable (means when we updgrade the version, the library can change or can 'breaking' our code )


## Pubspec
When we creating dart packages, the main file we need is pubspec.yaml
pubspec is the configuration for dart packages.
in pubspec we need to define the name of our dart packages and define all library we need. 

## Export library
After we create code in /src/ folder, we can create dart code in lib folder that used for exposing part that we want to expose
We can use ``export`` keyword if we want to exposing all code in the dart file, or we can use ``export show`` if only some part.
Dont forget to include ``library`` keyword and followed by our library name, even this is not required, but it is recommended to use because by default if we dont include ``library``, automatically the library name will be empty.  