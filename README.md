# EasyConstraint

EasyConstraint is a simple Swift library to add constraint to UI elements.

## Installation

Use the [Swift Package Manager](https://developer.apple.com/documentation/xcode/adding_package_dependencies_to_your_app) to install EasyConstraint.

```bash
https://github.com/bryanbarreto/easy-constraint
```

## Usage

```swift
import EasyConstraint

/* Primeiro, crie um elemento */
private lazy var button: UIButton = {
    let button = UIButton()
    button.setTitle("My Button", for: .normal)
    button.setTitleColor(.white, for: .normal)
    button.backgroundColor = .black
    return button
}()


/* Lembre- se de adicionar o seu botão como subview */
self.view.addSubview(self.button)


/* Agora basta escolher a melhor função para colocar constraints no seu elemento: */

/*
    anchor: É possível passar constraints para os 4 lados, 
    padding para os 4 lados, bem como width e height do elemento  
*/
self.button.anchor(top: self.view.topAnchor)


/* centerY: Alinha o elemento ao centro no eixo Y (vertical) */
self.button.centerY(self.view, padding: 30)

/* centerX: Alinha o elemento ao centro no eixo X (horizontal) */
self.button.centerX(self.view)

/* center: Alinha o elemento ao centro no eixo X e Y */
self.button.center(in: self.view, paddingX: 30, paddingY: 100)

/* fill: Faz o elemento ocupar todo o espaço disponível da view */
self.button.fill(in: self.view)
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)


