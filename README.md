SBFlatDatePicker
===============

SBFlatDatePicker is a customizable Flat Date Picker for iOS.

##Installation

Simply copy the source files into your project !

## UI

![ScreenShot] (http://imgur.com/MqKNP7d.jpg)

## Example Usage

``` objective-c
    //New view controller
    UIViewController *pickerViewController = [[UIViewController alloc] init];
    
    //Init the datePicker view and set self as delegate
    SBFlatDatePicker *datePicker = [[SBFlatDatePicker alloc] initWithFrame:self.view.bounds];
    [datePicker setDelegate:self];
    
    //Set the data picker as view of the new view controller
    [pickerViewController setView:datePicker];
    
    //Present the view controller
    [self presentViewController:pickerViewController animated:YES completion:nil];
``` 


##  Customization

``` objective-c
// The default settings are a date time picker with dates ranging from Today to 365+ (or one year) and minutes from 0-60

//You can set the phone to 24 hour mode by setting the property
    datePicker.twenthyFourHourMode = TRUE;

// You can customize the days or minutes with an NSIndexSet as follows

    //OPTIONAL - Choose Date Range (0 starts At today). 
    //Non continuous sets acceptable (use some enumeration) 
    datePicker.dayRange = [NSMutableIndexSet indexSetWithIndexesInRange:NSMakeRange(0, 60)]; //will show days ranging from today out for 60 days
    
    //OPTIONAL - Choose Minute  
    //Non continuous sets acceptable (use some enumeration for [indexSet addIndex:yourIndex];
    datePicker.minuterange = [NSMutableIndexSet indexSet];
    [datePicker.minuterange addIndex:0];
    [datePicker.minuterange addIndex:15];
    [datePicker.minuterange addIndex:30];
    [datePicker.minuterange addIndex:45];  //will only allow minute choices every quarter hour
    
    //Customize date format
    datePicker.dayFormat = @"EEE MMM dd";
    
    // Customize The Layout of The DatePicker column widths. The widths should add to the screen size (self.frame.size.width)
    datePicker.daysColumnXValue; // default is 0
    datePicker.daysColumnWidthValue;
    datePicker.hoursColumnWidthValue;
    datePicker.minColumnWidthValue;
    datePicker.meridianColumnWidth;

``` 



## Info
Inspired By MGConferenceDatePicker


## Contact

Solomon Bier
- http://github.com/SolomonBier
- https://angel.co/solomon-bier

## License

SBFlatDatePicker is available under the MIT license.
