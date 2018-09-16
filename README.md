# Pre_Work_Project_Lilly
My pre-work project for CodePath
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
        textLabel.text = textField.text
        textField.text = ""
        view.endEditing(true)
    }
    
    @IBAction func reset_Gesture(_ sender: Any) {
        textLabel.text = "Hello from Lilly"
        view.backgroundColor = backgroundColor
        textLabel.textColor = UIColor.black
    }
}
