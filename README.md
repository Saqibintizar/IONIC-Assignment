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
