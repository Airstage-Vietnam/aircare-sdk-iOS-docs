# AircareSDK

A simple SDK services with HealthKit

## Table of contents

- [AircareSDK](#aircaresdk)
  - [Table of contents](#table-of-contents)
  - [Data Types](#data-types)
    - [Characteristic identifiers](#characteristic-identifiers)
    - [Activity](#activity)
    - [Body measurements](#body-measurements)
    - [Reproductive health](#reproductive-health)
    - [Hearing](#hearing)
    - [Vital signs](#vital-signs)
    - [Alcohol consumption](#alcohol-consumption)
    - [Mobility](#mobility)
    - [Lab and test results](#lab-and-test-results)
    - [Mindfulness and sleep](#mindfulness-and-sleep)
    - [Self care](#self-care)
    - [UV exposure](#uv-exposure)
    - [Diving](#diving)
  - [Data types structure reference](#data-types-structure-reference)
  - [Integrating AircareSDK \& Apple HealthKit](#integrating-aircaresdk--apple-healthkit)
    - [Adding HealthKit to your app](#adding-healthkit-to-your-app)
  - [Adding a Package dependency](#adding-a-package-dependency)
  - [Accessing Sample Data in the Simulator (Deprecated)](#accessing-sample-data-in-the-simulator-deprecated)
    - [Overview (Deprecated)](#overview-deprecated)
    - [Add Sample Accounts (Deprecated)](#add-sample-accounts-deprecated)
    - [Current way to add sample accounts](#current-way-to-add-sample-accounts)
  - [Features list](#features-list)
    - [Common summary](#common-summary)
    - [Inject dependancy to application](#inject-dependancy-to-application)
    - [Heart rate management](#heart-rate-management)
    - [Step count management](#step-count-management)
    - [Distance walking, running management](#distance-walking-running-management)
    - [Active Energy Burned management](#active-energy-burned-management)

## Data Types

### Characteristic identifiers

- activityMoveMode: A characteristic identifier for the user’s activity mode.
- biologicalSex: A characteristic type identifier for the user’s sex.
- bloodType: A characteristic type identifier for the user’s blood type.
- dateOfBirth: A characteristic type identifier for the user’s date of birth.
- fitzpatrickSkinType: A characteristic type identifier for the user’s skin type.
- wheelchairUse: A characteristic identifier for the user’s use of a wheelchair.

### Activity

- stepCount:
A quantity sample type that measures the number of steps the user has taken.
- distanceWalkingRunning:
A quantity sample type that measures the distance the user has moved by walking or running.
- runningSpeed:
A quantity sample type that measures the runner’s speed.
- runningStrideLength:
A quantity sample type that measures the distance covered by a single step while running.
- runningPower:
A quantity sample type that measures the rate of work required for the runner to maintain their speed.
- runningGroundContactTime:
A quantity sample type that measures the amount of time the runner’s foot is in contact with the ground while running.
- runningVerticalOscillation:
A quantity sample type measuring pelvis vertical range of motion during a single running stride.
- distanceCycling:
A quantity sample type that measures the distance the user has moved by cycling.
- pushCount:
A quantity sample type that measures the number of pushes that the user has performed while using a wheelchair.
- distanceWheelchair:
A quantity sample type that measures the distance the user has moved using a wheelchair.
- swimmingStrokeCount:
A quantity sample type that measures the number of strokes performed while swimming.
- distanceSwimming:
A quantity sample type that measures the distance the user has moved while swimming.
- distanceDownhillSnowSports:
A quantity sample type that measures the distance the user has traveled while skiing or snowboarding.
- basalEnergyBurned:
A quantity sample type that measures the resting energy burned by the user.
- activeEnergyBurned:
A quantity sample type that measures the amount of active energy the user has burned.
- flightsClimbed:
A quantity sample type that measures the number flights of stairs that the user has climbed.
- nikeFuel:
A quantity sample type that measures the number of NikeFuel points the user has earned.
- appleExerciseTime:
A quantity sample type that measures the amount of time the user spent exercising.
- appleMoveTime:
A quantity sample type that measures the amount of time the user has spent performing activities that involve full-body movements during the specified day.
- appleStandTime:
A quantity sample type that measures the amount of time the user has spent standing.
- vo2Max:
A quantity sample that measures the maximal oxygen consumption during exercise.
- lowCardioFitnessEvent:
An event that indicates the user’s VO2 max values consistently fall below a particular aerobic fitness threshold.
- appleStandHour:
A category sample type that counts the number of hours in the day during which the user has stood and moved for at least one minute per hour.

### Body measurements

- height:
A quantity sample type that measures the user’s height.
- bodyMass:
A quantity sample type that measures the user’s weight.
- bodyMassIndex:
A quantity sample type that measures the user’s body mass index.
- leanBodyMass:
A quantity sample type that measures the user’s lean body mass.
- bodyFatPercentage:
A quantity sample type that measures the user’s body fat percentage.
- waistCircumference:
A quantity sample type that measures the user’s waist circumference.
- appleSleepingWristTemperature:
A quantity sample type that records the wrist temperature during sleep.

### Reproductive health

- menstrualFlow:
A category sample type that records menstrual cycles.
- intermenstrualBleeding:
A category sample type that records spotting outside the normal menstruation period.
- infrequentMenstrualCycles:
A category sample that indicates an infrequent menstrual cycle.
- irregularMenstrualCycles:
A category sample that indicates an irregular menstrual cycle.
- persistentIntermenstrualBleeding:
A category sample that indicates persistent intermenstrual bleeding.
- prolongedMenstrualPeriods:
A category sample that indicates a prolonged menstrual cycle.
- cervicalMucusQuality:
A category sample type that records the quality of the user’s cervical mucus.
- ovulationTestResult:
A category sample type that records the result of an ovulation home test.
- progesteroneTestResult:
A category type that represents the results from a home progesterone test.
- sexualActivity:
A category sample type that records sexual activity.
- contraceptive:
A category sample type that records the use of contraceptives.
- pregnancy:
A category type that records pregnancy.
- pregnancyTestResult:
A category type that represents the results from a home pregnancy test.
- lactation:
A category type that records lactation.
- basalBodyTemperature:
A quantity sample type that records the user’s basal body temperature.

### Hearing

- environmentalAudioExposure:
A quantity sample type that measures audio exposure to sounds in the environment.
- headphoneAudioExposure:
A quantity sample type that measures audio exposure from headphones.
- environmentalAudioExposureEvent:
A category sample type that records exposure to potentially damaging sounds from the environment.
- headphoneAudioExposureEvent:
A category sample type that records exposure to potentially damaging sounds from headphones.
- audioExposureEvent:
A category sample type for audio exposure events.

### Vital signs

- heartRate:
A quantity sample type that measures the user’s heart rate.
- lowHeartRateEvent:
A category sample type for low heart rate events.
- highHeartRateEvent:
A category sample type for high heart rate events.
- irregularHeartRhythmEvent:
A category sample type for irregular heart rhythm events.
- restingHeartRate:
A quantity sample type that measures the user’s resting heart rate.
- heartRateVariabilitySDNN:
A quantity sample type that measures the standard deviation of heartbeat intervals.
- heartRateRecoveryOneMinute:
A quantity sample that records the reduction in heart rate from the peak exercise rate to the rate one minute after exercising ended.
- atrialFibrillationBurden:
A quantity type that measures an estimate of the percentage of time a person’s heart shows signs of atrial fibrillation (AFib) while wearing Apple Watch.
- walkingHeartRateAverage:
A quantity sample type that measures the user’s heart rate while walking.
- oxygenSaturation:
A quantity sample type that measures the user’s oxygen saturation.
- bodyTemperature:
A quantity sample type that measures the user’s body temperature.
- bloodPressure:
A correlation sample that combines a systolic sample and a diastolic sample into a single blood pressure reading.
- bloodPressureSystolic:
A quantity sample type that measures the user’s systolic blood pressure.
- bloodPressureDiastolic:
A quantity sample type that measures the user’s diastolic blood pressure.
- respiratoryRate:
A quantity sample type that measures the user’s respiratory rate.

### Alcohol consumption

- bloodAlcoholContent:
A quantity sample type that measures the user’s blood alcohol content.
- numberOfAlcoholicBeverages:
A quantity sample type that measures the number of standard alcoholic drinks that the user has consumed.

### Mobility

- appleWalkingSteadiness:
A quantity sample type that measures the steadiness of the user’s gait.
- appleWalkingSteadinessEvent:
A category sample type that records an incident where the user showed a reduced score for their gait’s steadiness.
- sixMinuteWalkTestDistance:
A quantity sample type that stores the distance a user can walk during a six-minute walk test.
- walkingSpeed:
A quantity sample type that measures the user’s average speed when walking steadily over flat ground.
- walkingStepLength:
A quantity sample type that measures the average length of the user’s step when walking steadily over flat ground.
- walkingAsymmetryPercentage:
A quantity sample type that measures the percentage of steps in which one foot moves at a different speed than the other when walking on flat ground.
- walkingDoubleSupportPercentage:
A quantity sample type that measures the percentage of time when both of the user’s feet touch the ground while walking steadily over flat ground.
- stairAscentSpeed:
A quantity sample type measuring the user’s speed while climbing a flight of stairs.
- stairDescentSpeed:
A quantity sample type measuring the user’s speed while descending a flight of stairs.

### Lab and test results

- bloodAlcoholContent:
A quantity sample type that measures the user’s blood alcohol content.
- bloodGlucose:
A quantity sample type that measures the user’s blood glucose level.
- electrodermalActivity:
A quantity sample type that measures electrodermal activity.
- forcedExpiratoryVolume1:
A quantity sample type that measures the amount of air that can be forcibly exhaled from the lungs during the first second of a forced exhalation.
- forcedVitalCapacity:
A quantity sample type that measures the amount of air that can be forcibly exhaled from the lungs after taking the deepest breath possible.
- inhalerUsage:
A quantity sample type that measures the number of puffs the user takes from their inhaler.
- insulinDelivery:
A quantity sample that measures the amount of insulin delivered.
- numberOfTimesFallen:
A quantity sample type that measures the number of times the user fell.
- peakExpiratoryFlowRate:
A quantity sample type that measures the user’s maximum flow rate generated during a forceful exhalation.
- peripheralPerfusionIndex:
A quantity sample type that measures the user’s peripheral perfusion index.

### Mindfulness and sleep

- mindfulSession:
A category sample type for recording a mindful session.
- sleepAnalysis:
A category sample type for sleep analysis information.

### Self care

- toothbrushingEvent:
A category sample type for toothbrushing events.
- handwashingEvent:
A category sample type for handwashing events.

### UV exposure

- uvExposure:
A quantity sample type that measures the user’s exposure to UV radiation.

### Diving

- underwaterDepth:
A quantity sample that records a person’s depth underwater.
- waterTemperature:
A quantity sample that records the water temperature.

## Data types structure reference

- [HKQuantityType](https://developer.apple.com/documentation/healthkit/hkquantitytype)
- [HKCategoryType](https://developer.apple.com/documentation/healthkit/hkcategorytype)
- [HKStatistics](https://developer.apple.com/documentation/healthkit/hkstatistics)
- [HKSample](https://developer.apple.com/documentation/healthkit/hksample)


## Integrating AircareSDK & Apple HealthKit

### Adding HealthKit to your app

- Openup Xcode application in your mac and create a new ios project (HealthkitIntegration) with SwiftUI.(Using SwiftUI is not mandatory you can use UIKit as well with your requirement)
- Select your project name in Xcode and click on **Signing and Capabilities** tab.
- Then click on + **Capability**.

![img](/Docs/Assets/Images/1_A0CXf_bobCfMBoBTNDJmyw.png)

- Now serch for healthkit in the dilog appeared and click on HealthKit from search results.

![img](/Docs/Assets/Images/1_DST-IbY5ZIu-eSv4fHlD8Q.png)

- Now you will see that healthkit has been added to your project. Next go to info tab in same screen and add <ins>**NSHealthShareUsageDescription**</ins> under Custom iOS Target Properties.

![img](/Docs/Assets/Images/1_Csb7jAGQwFzJzNSO85XD1g.png)

- Here I have added message to the user that explains why the app requested permission to read samples from the HealthKit store. If you want to add write permission to apple health, you must add <ins>**NSHealthUpdateUsageDescription**</ins> similarly. Since I am going to write queries only to read data in this artivle I’ll add only <ins>**NSHealthShareUsageDescription**</ins> permission.

## Adding a Package dependency

- In Xcode, go to **File** → **Add Package Dependencies...** OR select your project in the Project Editor, go to the **Package Dependencies** tab, and press the + (plus).

- Enter a Package URL (e.g. a GitHub repository URL): <https://github.com/Airstage-Vietnam/aircare-sdk-iOS.git>

![img](/Docs/Assets/Images/5IpP5M44yY-900.jpeg)

- Click Add Package.

## Accessing Sample Data in the Simulator (Deprecated)

### Overview (Deprecated)

You cannot create your own HKClinicalRecord samples. When you need sample data to build or test your app, you must either download real data from a supported healthcare institution, or access existing sample data. Xcode provides three sample accounts in the simulator that you can use to build and test your app.

here are two steps to using the sample data:

- Add a sample account to provide the initial data for building and testing your app.

- Simulate updates by adding additional accounts.

### Add Sample Accounts (Deprecated)

- To access the sample accounts, open the Health app on the simulator, and navigate to Health Data > Health Records.

![img](/Docs/Assets/Images/3040233@2x.png)

- The Health Records view displays a message about adding accounts to healthcare institutions. Click Get Started. The system may ask to access your location, but you do not need to share that information in order to add the sample accounts. The system then shows the three sample accounts, and any supported healthcare institutions in your area if you shared your location.

![img](/Docs/Assets/Images/3040231@2x.png)

- Select the sample account you want to add, and the system displays the data available for that account. Select the data to add it to HealthKit.

![img](/Docs/Assets/Images/3040229@2x.png)

- Health then displays a confirmation showing that it has added the account to HealthKit. Click the Done button to continue, and the Health Records view shows the account that you added. You can add additional accounts, as needed.

![img](/Docs/Assets/Images/3040232@2x.png)

- Click on the account to view the data. You can browse all the clinical records associated with the account. This data is also available to your app while it is running on the simulator.

![img](/Docs/Assets/Images/3040228@2x.png)

### Current way to add sample accounts

- While the screenshots are out of date, the sample data is still there. In the Health app, use the "Browse" tab, scroll all the way to the bottom and select "Add Account". Then you'll see the 3 sample accounts show up and you can take it from there.

- Note that you need your device to be set to US, CA or GB locales for the "Add Account" buttons to show up.

## Features list

### Common summary

- Create startDate, endDate and date format

```
// Create startDate and endDate with current timezone
let endDate = Date()
var startDate = Calendar.current.date(byAdding: .month, value: -1, to: endDate)
startDate = Calendar.current.date(bySettingHour: 0, minute: 0, second: 0, of: startDate!)

let dateFormatter = DateFormatter()
dateFormatter.timeZone = .current
dateFormatter.dateFormat = "yyyy-MM-dd HH:mm:ss Z"

// Convert startDate and endDate to current timezone
let startDateCurrentTimeZone = dateFormatter.date(from: dateFormatter.string(from: startDate!))!
let endDateCurrentTimeZone = dateFormatter.date(from: dateFormatter.string(from: endDate))!
```

- Create sort descriptor

```
// Init sort descriptor
let sortDescriptor = NSSortDescriptor(key: HKSampleSortIdentifierEndDate, ascending: false)
```

- Common handle errors features func return
  
```
fatalError("Error during query: \(String(describing: error))")
```

### Inject dependancy to application

- At root as application you must import HealthKit and AircareSDK, after you initialize the service.

```
import HealthKit
import AircareSDK
...
@StateObject var manage = AircareManager()
...
```

- At first time you run application, if you initialize AircareSDK service it will be automatically request permission health app.

### Heart rate management

- Unit of heart rate: count/min (BPM)

```
let heartRateUnit = HKUnit(from: "count/min")
```

- Protocol structures

```
    // You use this function to get today heart rate.
    func getTodayHeartRate(_ healthStore: HKHealthStore, quantityType: HKQuantityType, sortDescriptor: NSSortDescriptor, withEnterUserData: Bool, with completion: @escaping (HKSample?) -> Void)
    
    // You use this function to get latest heart rate.
    func getLatestHeartRate(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, sortDescriptor: NSSortDescriptor,   with completion: @escaping ([HKSample]?) -> Void)
    
    // You use this function to get list heart rate in range with startDate and endDate.
    func getHeartRateInRange(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, sortDescriptor: NSSortDescriptor,  with completion: @escaping ([HKSample]?) -> Void)
```

- How get today heart rate

```
...
func getTodayHeartRate() {
        // Heart rate type
        guard let heartRateType = HKObjectType.quantityType(forIdentifier: .heartRate) else {
            return
        }

        // Execute query list of heart rate in range with startDate and endDate
        manager.heartRateManager.getTodayHeartRate(manager.healthStore, quantityType: heartRateType, sortDescriptor: sortDescriptor, withEnterUserData: true) { (results) in

            // Write data logic code here
            ...
            ...
            ...
            // Example

            let data = results? as! HKQuantitySample
            let unit = HKUnit(from: "count/min")
            let latestHeartRate = data.quantity.doubleValue(for: unit)

            // Log latest heart rate data
            print("Start Date: \(String(describing: dateFormatter.string(from: data.startDate))), End Date: \(String(describing: dateFormatter.string(from: data.endDate))) -- HeartRate: \(latestHeartRate) BPM")

            // Create activity component UI
            let activity = Activity(id: "1", title: "Today Heart rate", subTitle: "Nothing", image: "heart.fill", amount: "\(latestHeartRate)")
            activities["todayHeartRate"] = activity
        }
    }
...
```

- How get list latest heart rate

```
...
func getLatestHeartRate() {
        // Heart rate type
        guard let heartRateType = HKObjectType.quantityType(forIdentifier: .heartRate) else {
            return
        }
        
        // Execute query list of heart rate in range with startDate and endDate
        manager.heartRateManager.getLatestHeartRate(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: heartRateType, sortDescriptor: sortDescriptor, withEnterUserData: true) { (results) in
            
            // Write data logic code here
            ...
            ...
            ...
            // Example

            let data = results?[0] as! HKQuantitySample
            let unit = HKUnit(from: "count/min")
            let latestHeartRate = data.quantity.doubleValue(for: unit)

            // Log latest heart rate data
            print("Start Date: \(String(describing: dateFormatter.string(from: data.startDate))), End Date: \(String(describing: dateFormatter.string(from: data.endDate))) -- HeartRate: \(latestHeartRate) BPM")

            // Create activity component UI
            let activity = Activity(id: "1", title: "Today Heart rate", subTitle: "Nothing", image: "heart.fill", amount: "\(latestHeartRate)")
            activities["todayHeartRate"] = activity
        }
    }
...
```

- How get list in range heart rate

```
...
func getHeartRateInRange() {
        // Heart rate type
        guard let heartRateType = HKObjectType.quantityType(forIdentifier: .heartRate) else {
            return
        }
        
        // Convert startDate and endDate to current timezone
        let startDateCurrentTimeZone = dateFormatter.date(from: dateFormatter.string(from: startDate!))!
        let endDateCurrentTimeZone = dateFormatter.date(from: dateFormatter.string(from: endDate))!
        
        // Execute query list of heart rate in range with startDate and endDate
        manager.heartRateManager.getHeartRateInRange(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: heartRateType, sortDescriptor: sortDescriptor, withEnterUserData: true) { (results) in
            
            // Write data logic code here
            ...
            ...
            ...
            // Example

            let data = results?[0] as! HKQuantitySample
            let unit = HKUnit(from: "count/min")
            let latestHeartRate = data.quantity.doubleValue(for: unit)

            // Log latest heart rate data
            print("Start Date: \(String(describing: dateFormatter.string(from: data.startDate))), End Date: \(String(describing: dateFormatter.string(from: data.endDate))) -- HeartRate: \(latestHeartRate) BPM")

            // Create activity component UI
            let activity = Activity(id: "1", title: "Today Heart rate", subTitle: "Nothing", image: "heart.fill", amount: "\(latestHeartRate)")
            activities["todayHeartRate"] = activity
        }
    }
...
```

### Step count management

- Unit of step count: step (Step)

```
let distanceUnit = HKUnit.count()
```

- Protocol structures

```
    // You use this function to get today step count.
    func getTodayStepCount(_ healthStore: HKHealthStore, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get latest step count.
    func getLatestStepCount(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get list step count in range with startDate and endDate.
    func getStepCountInRange(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
```

- How get today step count

```
...
func getTodayStepCount() {
        // Step count type
        guard let stepCountType = HKObjectType.quantityType(forIdentifier: .stepCount) else {
            return
        }
       
        // Execute query sum step count from 00:00 AM to now
        manager.stepCountManager.getTodayStepCount(manager.healthStore, quantityType: stepCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // step count data
            let stepCount = quatity.doubleValue(for: .count())

            // Log step count data
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- StepCount: \(round(Double(stepCount))) Step")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Step", subTitle: "Goal: 10,000 Step", image: "figure.walk", amount: "\(round(Double(stepCount)))", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todaySteps"] = activity
        }
    }
...
```

- How get latest step count

```
...
func getLatestStepCount() {
        // Step count type
        guard let stepCountType = HKObjectType.quantityType(forIdentifier: .stepCount) else {
            return
        }
             
        // Execute query sum step count from startDate to endDate
        manager.stepCountManager.getLatestStepCount(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: stepCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // step count data
            let stepCount = quatity.doubleValue(for: .count())

            // Log step count data
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- StepCount: \(round(Double(stepCount))) Step")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Step", subTitle: "Goal: 10,000 Step", image: "figure.walk", amount: "\(round(Double(stepCount)))", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todaySteps"] = activity
        }
    }
...
```

- How get in range step count

```
...
func getStepCountInRange() {
        // Step count type
        guard let stepCountType = HKObjectType.quantityType(forIdentifier: .stepCount) else {
            return
        }
  
        // Execute query sum step count from startDate to endDate
        manager.stepCountManager.getStepCountInRange(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: stepCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // step count data
            let stepCount = quatity.doubleValue(for: .count())

            // Log step count data
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- StepCount: \(round(Double(stepCount))) Step")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Step", subTitle: "Goal: 10,000 Step", image: "figure.walk", amount: "\(round(Double(stepCount)))", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todaySteps"] = activity
        }
    }
...
```

### Distance walking, running management

- Unit of distance walking, running: mile (Mile)

```
let distanceUnit = HKUnit.mile()
```

- Protocol structures

```
    // You use this function to get today distance walking, running.
    func getTodayDistanceWalkingRunning(_ healthStore: HKHealthStore, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get latest distance walking, running.
    func getLatestDistanceWalkingRunning(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get list distance walking, running in range with startDate and endDate.
    func getDistanceWalkingRunningInRange(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
```

- How get today distance walking, running

```
...
func getTodayDistance() {
        // Distance type
        guard let distanceWalkingRunningType = HKObjectType.quantityType(forIdentifier: .distanceWalkingRunning) else {
            return
        }
        
        // Execute query sum distance walking, running from startDate to endDate
        manager.distanceWalkingRunningManager.getTodayDistanceWalkingRunning(manager.healthStore, quantityType: distanceWalkingRunningType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // distance walking, running data
            let distance = quatity.doubleValue(for: HKUnit.mile())

            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- DistanceWalkingRunning: \(round(Double(distance))) Mile")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Walking", subTitle: "Goal: 10 Km", image: "figure.walk", amount: "\(round(Double(distance.convert(from: .miles, to: .meters) / 1000))) Km", startDate: dateFormatter.string(from: results!.startDate), endDate: dateFormatter.string(from: results!.endDate))
            activities["todayDistanceWalkingRunning"] = activity
        }
    }
...
```

- How get latest distance walking, running

```
...
func getLatestDistance() {
        // Distance type
        guard let distanceWalkingRunningType = HKObjectType.quantityType(forIdentifier: .distanceWalkingRunning) else {
            return
        }
        
        // Execute query sum distance walking, running from startDate to endDate
        manager.distanceWalkingRunningManager.getLatestDistanceWalkingRunning(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: distanceWalkingRunningType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // distance walking, running data
            let distance = quatity.doubleValue(for: HKUnit.mile())

            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- DistanceWalkingRunning: \(round(Double(distance))) Mile")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Walking", subTitle: "Goal: 10 Km", image: "figure.walk", amount: "\(round(Double(distance.convert(from: .miles, to: .meters) / 1000))) Km", startDate: dateFormatter.string(from: results!.startDate), endDate: dateFormatter.string(from: results!.endDate))
            activities["todayDistanceWalkingRunning"] = activity
        }
    }
...
```

- How get in range distance walking, running

```
...
func getDistanceInRange() {
        // Distance type
        guard let distanceWalkingRunningType = HKObjectType.quantityType(forIdentifier: .distanceWalkingRunning) else {
            return
        }
        
        // Execute query sum distance walking, running from startDate to endDate
        manager.distanceWalkingRunningManager.getDistanceWalkingRunningInRange(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: distanceWalkingRunningType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // distance walking, running data
            let distance = quatity.doubleValue(for: HKUnit.mile())

            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- DistanceWalkingRunning: \(round(Double(distance))) Mile")

            // Create activity component UI
            let activity = Activity(id: "0", title: "Today Walking", subTitle: "Goal: 10 Km", image: "figure.walk", amount: "\(round(Double(distance.convert(from: .miles, to: .meters) / 1000))) Km", startDate: dateFormatter.string(from: results!.startDate), endDate: dateFormatter.string(from: results!.endDate))
            activities["todayDistanceWalkingRunning"] = activity
        }
    }
...
```

### Active Energy Burned management

- Unit of Active Energy Burned: kcal (Kcal)

```
let activeEnergyBurnedUnit = HKUnit.kilocalorie()
```

- Protocol structures

```
    // You use this function to get today energy burned.
    func getTodayActiveEnergyBurned(_ healthStore: HKHealthStore, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get latest energy burned.
    func getLatestActiveEnergyBurned(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
    
    // You use this function to get list energy burned in range with startDate and endDate.
    func getActiveEnergyBurnedInRange(_ healthStore: HKHealthStore, startDate: Date, endDate: Date, quantityType: HKQuantityType, withEnterUserData: Bool, with completion: @escaping (HKStatistics?) -> Void)
```

- How get today Active Energy Burned

```
...
func getTodayActiveEnergyBurned() {
        // Active Energy Burned type
        guard let activeEnergyBurnedCountType = HKObjectType.quantityType(forIdentifier: .activeEnergyBurned) else {
            return
        }
        
        // Execute query sum Active Energy Burned from startDate to endDate
        manager.activeEnergyBurnedManager.getTodayActiveEnergyBurned(manager.healthStore, quantityType: activeEnergyBurnedCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // Active Energy Burned data
            let activeEnergyBurned = quatity.doubleValue(for: HKUnit.kilocalorie())
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- ActiveEnergyBurned: \(round(Double(activeEnergyBurned))) Kcal")

            // Create activity component UI
            let activity = Activity(id: "4", title: "Today Calories Burned", subTitle: "Goal: 1,000 Kcal", image: "figure.walk", amount: "\(round(Double(activeEnergyBurned))) Kcal", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todayActiveEnergyBurned"] = activity
        }
    }
...
```

- How get latest Active Energy Burned

```
...
func getLatestActiveEnergyBurned() {
        // Active Energy Burned type
        guard let activeEnergyBurnedCountType = HKObjectType.quantityType(forIdentifier: .activeEnergyBurned) else {
            return
        }
        
        // Execute query sum Active Energy Burned from startDate to endDate
        manager.activeEnergyBurnedManager.getLatestActiveEnergyBurned(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: activeEnergyBurnedCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }

            // Write data logic code here
            ...
            ...
            ...
            // Example
            
            // Active Energy Burned data
            let activeEnergyBurned = quatity.doubleValue(for: HKUnit.kilocalorie())
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- ActiveEnergyBurned: \(round(Double(activeEnergyBurned))) Kcal")

            // Create activity component UI
            let activity = Activity(id: "4", title: "Today Calories Burned", subTitle: "Goal: 1,000 Kcal", image: "figure.walk", amount: "\(round(Double(activeEnergyBurned))) Kcal", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todayActiveEnergyBurned"] = activity
        }
    }
...
```

- How get in range Active Energy Burned

```
...
func getActiveEnergyBurnedInRange() {
        // Active Energy Burned type
        guard let activeEnergyBurnedCountType = HKObjectType.quantityType(forIdentifier: .activeEnergyBurned) else {
            return
        }
        
        // Execute query sum Active Energy Burned from startDate to endDate
        manager.activeEnergyBurnedManager.getActiveEnergyBurnedInRange(manager.healthStore, startDate: startDateCurrentTimeZone, endDate: endDateCurrentTimeZone, quantityType: activeEnergyBurnedCountType, withEnterUserData: true) { (results) in
            guard let quatity = results?.sumQuantity() else {
                return
            }
            
            // Write data logic code here
            ...
            ...
            ...
            // Example

            // Active Energy Burned data
            let activeEnergyBurned = quatity.doubleValue(for: HKUnit.kilocalorie())
            print("Start Date: \(String(describing: dateFormatter.string(from: results!.startDate))), End Date: \(String(describing: dateFormatter.string(from: results!.endDate))) -- ActiveEnergyBurned: \(round(Double(activeEnergyBurned))) Kcal")

            // Create activity component UI
            let activity = Activity(id: "4", title: "Today Calories Burned", subTitle: "Goal: 1,000 Kcal", image: "figure.walk", amount: "\(round(Double(activeEnergyBurned))) Kcal", startDate: dateFormatter.string(from: startDateCurrentTimeZone), endDate: dateFormatter.string(from: endDateCurrentTimeZone))
            activities["todayActiveEnergyBurned"] = activity
        }
    }
...
```
