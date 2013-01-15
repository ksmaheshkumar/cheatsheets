**Listing 5.16** Additions to .autotest needed to run integration tests with Autotest on OS X.


**Model settings:**

	validates :email, :presence => true,
		:format => { :with => email_regex },
		:uniqueness => { :case_sensitive => false}

**Migration to add email uniqueness:**

	add_index :users, :email, :unique => true



	



		end
		
		it "should reject duplicate email addresses" do



				User.new(@attr.merge(:password_confirmation => "invalid")).should_not be_valid
				User.new(hash).should_not be_valid

				User.new(hash).should_not be_valid



				@user.should respond_to(:encrypted_password)






	attr_accessible :name, :email, :password, :password_confirmation
	
	# Automatically create the virtual attribute 'password_confirmation'.
	validates :password, :presence => true,
**Add `encrypted_password` to `User` model**

	rails generate migration add_password_to_users encrypted_password:string
**Run specific RSpec test**

	rspec spec/models/user_spec.rb \
**`before_save` callback to save `encrypted_password` in model `User`**

	before_save :encrypt_password
**Authenticate logins**

	describe "authenticate method" do
			wrong_password_user = User.authenticate(@attr[:email], "wrongpass")
			wrong_password_user.should be_nil
			nonexistent_user = User.authenticate("bar@foo.com", @attr[:password])
			nonexistent_user.should be_nil


	end
**Class method to find users**

	def self.authenticate(email, submitted_password)
Install `factory_girl_rails`

	gem 'factory_girl_rails', '1.0'
	
`spec/factories.rb`

	# Using the symbol ':user', we get Factory Girl to simulate the User model.

`spec/controllers/users_controller_spec.rb`






