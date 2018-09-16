## Application name: My first IOS mobile application

### App Description
My IOS mobile application allows for simple user interaction features. User can change color of the label from black to blue, change the color of the app background from light pink to cyan and change the text string of the label. If user taps the view background, the app will reset all views to how they originally appear.   

### App Walk-though

<img src="http://recordit.co/Vo8VKhxPt2" width=200><br>

### Required User Stories
- [X] 1. User sees custom text in a label - Hello from {name}!
- [X] 2. User see's custom background color.
- [X] 3. User can tap a button to change the text color of the label.

### Optional User Stories
- [X] 1. User can tap a button to change the color of the background view.
- [X] 2. User can tap a button to change the text string of the label - Goodbye 👋.
- [X] 3. User can tap on the background view to reset all views to default settings.
- [X] 4. User can update the label text with custom text entered into the text field.
   - [X] a. User can enter text into a text field using the keyboard.
   - [X] b. User can tap the "Change text string" button to update the label with the text from the text field.
   - [X] c. If the text field is empty, update label with default text string.
   - [X] d. The keyboard is dismissed after the button has been tapped.





//
//  ViewController.swift
//  Pre_Work_Project_Lilly_Zhou
//
//  Created by Lilly Zhou on 9/15/18.
//  Copyright © 2018 Lilly Zhou. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

    
    @IBOutlet weak var textLabel: UILabel!
    
    @IBOutlet weak var textField: UITextField!
    
    var backgroundColor: UIColor!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
        backgroundColor = view.backgroundColor
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    @IBAction func didTapButton(_ sender: Any) {
       textLabel.textColor = UIColor.blue
    }
    
    @IBAction func didTapViewButton(_ sender: Any) {
        view.backgroundColor = UIColor.cyan
    }
    
    @IBAction func didTapChangeString(_ sender: Any) {
        if(textField.text == ""){
            textLabel.text = "Hello from Lilly"
        } else {
        textLabel.text = textField.text
        textField.text = ""
        }
        view.endEditing(true)
    }
    
    @IBAction func reset_Gesture(_ sender: Any) {
        textLabel.text = "Hello from Lilly"
        view.backgroundColor = backgroundColor
        textLabel.textColor = UIColor.black
    }
}
