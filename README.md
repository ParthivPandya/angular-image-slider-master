angular-image-slider
Slider based on Angular 2+, currently supports Angular 8

Description
This project is my tiny attempt to publish my first node package. I may not continue to support this package. But lets see! Let me know, if you want to have new features. Thanks.

Installation
To install this module to an external project, follow the procedure:

npm install angular-image-slider --save

Add SliderModule and BrowserAnimationsModule import to your @NgModule like example below.

import { BrowserModule } from "@angular/platform-browser";
import { BrowserAnimationsModule } from "@angular/platform-browser/animations";
import { NgModule } from "@angular/core";

import { AppComponent } from "./app.component";
import { SliderModule } from "angular-image-slider";

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule, BrowserAnimationsModule, SliderModule],
  providers: [],
  bootstrap: [AppComponent],
})
export class AppModule {}
Usage
You just need to construct a simple array containing image urls.

import { Component } from "@angular/core";

@Component({
  selector: "app-root",
  templateUrl: "./app.component.html",
  styleUrls: ["./app.component.css"],
})
export class AppComponent {
  public imagesUrl;

  ngOnInit() {
    this.imagesUrl = ["IMAGE_URL1.jpg", "IMAGE_URL2.jpg", "IMAGE_URL3.jpg"];
  }
}
Use array as an input for 'images' in the slider component. Array should contain url links:

<angular-image-slider [images]="imagesUrl"></angular-image-slider>
You can configure the slider to auto rotate. You can also decide the autoRotate speed and the direction, as well as number of images that is displayed initially by default.

<angular-image-slider
  [autoRotate]="false"
  [autoRotateAfter]="0"
  [autoRotateRight]="false"
  [imagesToBeDisplayedByDefault]="3"
  [images]="imagesUrl"
></angular-image-slider>

Demo
Online demo is here

Github:
https://github.com/ParthivPandya/angular-image-slider-master

Package:
https://github.com/ParthivPandya/angular-image-slider-master

License
License: MIT
Author
Author: parthivpandya
Keywords
Angular
Angular2
Angular 2+
Image Slider
Carousel
Slider
 
