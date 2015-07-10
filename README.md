# UIImageGenerator

UIImageGenerator is a Swift script generating a single Swift file with UIImage category containing all the imagese from .xcassetts files.

### Example

```

// ******************************************** 
// ** Autogenerated file from UIImageGenerator
// ********************************************

	import UIKit
	
	extension UIImage { 
	
	   // Images
	   struct Images {
	       static let closeButton = UIImage(named: "close-button")
	       static let commentCellArrow = UIImage(named: "comment-cell-arrow")
	       static let commentsIcon = UIImage(named: "comments-icon")
	       static let defaultAppBackground = UIImage(named: "default-app-background")
	       static let disclosure = UIImage(named: "disclosure")
	       static let loadingIndicatorBackground = UIImage(named: "loading-indicator-background")
	       static let loadingIndicatorWheel = UIImage(named: "loading-indicator-wheel")
	       static let muteButtonMuted = UIImage(named: "mute-button-muted")
	       static let muteButton = UIImage(named: "mute-button")
	       static let pauseButton = UIImage(named: "pause-button")
	       static let playButton = UIImage(named: "play-button")
	       static let playIcon = UIImage(named: "play-icon")
	       static let questionMarkButton = UIImage(named: "question-mark-button")
	       static let searchButton = UIImage(named: "search-button")
	       static let showDefaultIcon = UIImage(named: "show-default-icon")
	       static let systemTapperProfileImage = UIImage(named: "system-tapper-profile-image")
	       static let tapperPlaceholder = UIImage(named: "tapper-placeholder")
	       static let tappersIcon = UIImage(named: "tappers-icon")
	       static let tmpIcon = UIImage(named: "tmp_icon")
	       static let twitterFavoriteButton = UIImage(named: "twitter-favorite-button")
	       static let twitterLogo = UIImage(named: "twitter-logo")
	       static let twitterReplyButton = UIImage(named: "twitter-reply-button")
	       static let twitterRetweetButton = UIImage(named: "twitter-retweet-button")
	   }
	
	   // OnboardingImages
	   struct OnboardingImages {
	       static let onboardingIconCheckmark = UIImage(named: "onboarding-icon-checkmark")
	       static let onboardingIconNotification = UIImage(named: "onboarding-icon-notification")
	       static let onboardingPagerStepOne = UIImage(named: "onboarding-pager-step-one")
	       static let onboardingPagerStepThree = UIImage(named: "onboarding-pager-step-three")
	       static let onboardingPagerStepTwo = UIImage(named: "onboarding-pager-step-two")
	       static let step1Background = UIImage(named: "step-1-background")
	       static let step2Background = UIImage(named: "step-2-background")
	       static let step2Hand = UIImage(named: "step-2-hand")
	       static let step3Hand = UIImage(named: "step-3-hand")
	       static let wiretapLogoWithText = UIImage(named: "wiretap-logo-with-text")
	   }
	}
```



### How to use it

- Copy the ```UIImageGenerator.swift``` file to ```/usr/local/bin/``` of your computer

- Add following lines to the **Run Script** phase of you Xcode project target settings.

```
	if [ "${CONFIGURATION}" != "Release" ]; then
	IMAGE_GENERATOR="/usr/local/bin/UIImageGenerator.swift"
    if [ -f "$IMAGE_GENERATOR" ]; then
    echo "Image Generator"
    $IMAGE_GENERATOR "$PROJECT_DIR/$PROJECT_NAME" > "$PROJECT_DIR/$PROJECT_NAME/ProjectImages.swift"
    fi
    fi
```

- Add the ```ProjectImages.swift``` file to your project.

- You can then use all your images this way:


	``` let image = UIImage.OnboardingImages.step2Hand ```




### See also

[Natalie - Storyboard Code Generator (for Swift)](https://github.com/krzyzanowskim/Natalie)

[Swift Scripting talk by Ayaka Nonaka](https://realm.io/news/swift-scripting/)
