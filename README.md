
# Liferay Development Properties

This branch contains essential properties for Liferay development.
These properties can be used to configure your Liferay development environment and make development more efficient.

## Configuration

The following properties are included in the configuration:

## Developer Properties
```
include-and-override=portal-developer.properties
com.liferay.portal.upload.UploadServletRequestImpl.max.size=2147483648
com.liferay.portal.upload.LiferayFileItem.threshold.size=2147483648
company.security.update.password.required=false
company.security.strangers.verify=true
passwords.default.policy.change.required=false
```

### Admin Email Configuration

```properties
admin.email.from.address=test@liferay.com
admin.email.from.name=Test Test
```

### Database Configuration (Example for PostgreSQL)

```properties
jdbc.default.driverClassName=org.postgresql.Driver
jdbc.default.password=postgres
jdbc.default.url=jdbc:postgresql://localhost:5432/
jdbc.default.username=postgres
```

### Other Settings

```properties
company.default.locale=en_US
company.default.time.zone=UTC
company.default.web.id=liferay.com
default.admin.email.address.prefix=test
setup.wizard.enabled=false
```

## Usage

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/liferay-development-properties.git
```

Copy the properties from `portal-developer.properties` and paste them into your Liferay `portal-ext.properties` file or create a new configuration file.

Modify the values as needed for your specific development environment.

Save the changes and restart your Liferay instance.

## Contributing

If you have suggestions for additional properties or improvements, feel free to open an issue or submit a pull request.

Happy coding!
```
Feel free to use this content as a template for your README.md file.
Adjust any placeholders like `yourusername` with your actual GitHub username.
