(HTML FILE)

<!--
  Generated template for the LoginPage page.

  See http://ionicframework.com/docs/components/#navigation for more info on
  Ionic pages and navigation.
-->
<ion-header>

  <ion-navbar>
    <ion-title>Login Form</ion-title>
  </ion-navbar>

</ion-header>


<ion-content padding>

  <ion-list>
    <ion-item>
      <ion-label floating>Username</ion-label>
      <ion-input [(ngModel)]="username" type="text"></ion-input>
    </ion-item>

    <ion-item>
        <ion-label floating>Email</ion-label>
        <ion-input [(ngModel)]="Email" type="text"></ion-input>
    </ion-item> 
    
    <ion-item>
      <ion-label floating>Password</ion-label>
      <ion-input [(ngModel)]="password" type="password"></ion-input>
  </ion-item> 
  </ion-list>  

  <div padding>
    <button ion-button block (click)="login()">Login</button>
  </div> 

  <div padding>
    <button ion-button block (click)="login()">Cancel</button>
  </div> 

</ion-content>



(TS FILE)

import { Component } from '@angular/core';
import { IonicPage, NavController, NavParams, AlertController } from 'ionic-angular';

/**
 * Generated class for the LoginPage page.
 *
 * See https://ionicframework.com/docs/components/#navigation for more info on
 * Ionic pages and navigation.
 */

@IonicPage()
@Component({
  selector: 'page-login',
  templateUrl: 'login.html',
})
export class LoginPage {

  username : string;
  password : string;

  constructor(public navCtrl: NavController, public navParams: NavParams, public alertCtrl: AlertController) {
  }

  login(){
    if(this.username == "noman" && this.password =="noman123"){
      const alert = this.alertCtrl.create({
        title: 'Success!',
        subTitle: 'Successfully logged In',
        buttons: ['OK']
      });
      alert.present();
    }else{
      const alert = this.alertCtrl.create({
        title: 'Error!',
        subTitle: 'Incorrent Username or Password',
        buttons: ['OK']
      });
      alert.present();
    }
  }
}

