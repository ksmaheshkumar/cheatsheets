Print to log

	NSLog(@“Log message”);

AppDelete.m

	# get mainscreen bounds
	CGRect viewRect = [[UIScreen mainScreen] bounds];
	
	# print screen height and width to NSLog
	NSLog(@"Screen is %f tall and %f wide",
                 viewRect.size.height, viewRect.size.width); 
                 
	# Allocate memory for a UI Window and initialize object with 
	# frame size to the bounds of the main screen
	UIWindow *window = [[UIWindow alloc] initWithFrame:viewRect];
	
	# or
	self.window = [[UIWindow alloc] initWithFrame:viewRect];
	
	# Application windows are expected to have a root view controller 
	# at the end of application launch

	# setup view background color



AppDelete.h

	@property (strong, nonatomic) UIWindow *window;



		UIButton *firstButton = [UIButton buttonWithType:UIButtonTypeRoundedRect];
		# Located at x = 100pts, y = 100pts, 100pts width, 44pts height
		firstButton.frame = CGRectMake(100, 100, 100, 44);
		
		# Sets the title when pressed >> forState:UIControlStateHighlighted
		[firstButton setTitle:@"Click me!" forState:UIControlStateNormal];
		
		[self.view addSubview:firstButton];
		
		UILabel *firstLabel = [[UILabel alloc] initWithFrame:CGRectMake(50, 30, 200, 44)];
		firstLabel.backgroundColor = [UIColor clearColor];
		firstLabel.text = @"Hello, welcome to my app!";
		[self.view addSubview:firstLabel];
		
		# addTarget:self >> # ViewController
		[firstButton addTarget:self 


