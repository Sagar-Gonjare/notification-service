Data Completeness Rule:
This rule examines the NotificationRequest object to ensure that all required fields (mode, subject, body, to) are non-null. If any of these fields are found to be null, the rule generates a NotificationResponse object with the appropriate error status, code, and message, signaling incomplete data.

Valid Mode Rule:
This rule validates the specified mode in the NotificationRequest object. It confirms that the mode is not null and matches one of the values defined in the EmailConstant enum. In the case of an invalid mode, the rule produces a NotificationResponse object containing an error status, code, and message indicating the presence of an invalid mode.

Email Format Validity Rule:
This rule specifically targets cases where the notification mode is set to "EMAIL" and checks whether the email address provided in the to field of the NotificationRequest object adheres to a valid email format. If the email format is found to be invalid, the rule generates a NotificationResponse object with the relevant error status, code, and message, signaling an issue with the email format.
