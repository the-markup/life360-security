# How We Tested the Account Security of Life360

This contains the data for our story "[Family Safety App Touting Digital Security Leaves Its Own Users' Sensitive Data at Risk](https://themarkup.org/privacy/2022/02/17/family-safety-app-touting-digital-security-leaves-its-own-users-sensitive-data-at-risk)."

The Markup tested the Life360 app against a series of standards published by the Open Web Application Security Project (OWASP), a nonprofit foundation that promotes app security standards. The organization’s [Application Security Verification Standard](https://github.com/owasp/asvs/) (ASVS) are voluntary industry guidelines and also closely follow the [National Institute of Standards and Technology’s Digital Identity Guidelines](https://pages.nist.gov/800-63-3/), which are federal standards for user authentication. 

We found that Life360’s app failed to pass six of the 19 tests we were able to conduct for important security features such as limiting failed log-in attempts and verifying that passwords are checked against a set of breached credentials. Life360 did pass 11 other of the ASVS tests—for example we verified that users are able to change their password and can use  passwords of more than 64 characters. Life360 partially passed two additional tests that check if a user is notified about account changes. We found the app notified users about log-ins from multiple devices and password reset requests but not when the account’s email address, phone number, or password were changed. You can see the full results of our testing in our [data](https://github.com/the-markup/life360-security/blob/main/life360_security_test.csv).

## What standards did we use for testing?

After speaking with security experts, we decided to use OWASP’s Application Security Verification Standard (ASVS) Version 4.0.3, the latest version when we began our tests.  

The ASVS sets forth “Application Security Verification Levels” that rank the importance of security for a given application, depending on the type of data managed and how sensitive the use case is. Jim Manico, the ASVS’s project manager, told us that Life360 would easily fall into ASVS Level 2, which according to the standard’s documentation is for “applications that contain sensitive data, which requires protection and is the recommended level for most apps.” 

The ASVS sections we focused on were:

- V2.1 Password Security
- V2.2 General Authenticator Security
- V2.5 Credential Recovery

We identified 19 tests from these sections that we were able to apply to Life360’s user account security. 

In addition to testing logging in to life360.com on a desktop computer, our tests were conducted on the following devices: 

- Samsung Galaxy S10, Android 10, Life360 App version 21.12.1
- iPhone XS - iOS 15.2; Life360 App version 21.12.20

Our tests were conducted between December 2021 and February 2022. 

## Limitations

Our scope for this story was user account security, and there are only certain tests we could run as end users of Life360’s platform. We only chose tests that we would be able to run on our accounts, on the iOS and Android Life360 apps and Life360.com. 

We made a robust effort to apply each of these tests to Life360’s platform, but it is possible there are user authentication flows that we did not encounter. 

## Test results
We assigned each score one of four outcomes:

- **PASSED** - The test was clearly applied to the app, and we could observe a clear result. 
- **FAILED** - The test was clearly not passed, and the app did not meet the criteria described for the rule.
- **MIXED** - Some of the conditions passed, and some failed. 
- **N/A** - Not applicable. We could not apply this test to the app. 


## Data  

<table border="0" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Section</strong></td>
      <td>The subsection of OWASP’s Application Security Verification Standards (ASVS) Version 4.0.3
</td>
    </tr>
     <tr>
      <td><strong>Test</strong></td>
      <td>The individual test number from the standard.</td>
    </tr>
      <tr>
      <td><strong>Description</strong></td>
      <td>The description of the test as it appears in the standard.</td>
    </tr>
     <tr>
     <td><strong>Description of test</strong></td>
      <td>How we chose to apply the test to Life360’s platform.</td>
    </tr>
     <tr>
     <td><strong>Result of test</strong></td>
      <td>Our determination of how Life360 did in the test.</td>
    </tr>
  </tbody>
</table>


[life360_security_test.csv](https://github.com/the-markup/life360-security/blob/main/life360_security_test.csv) - 11.1 KB. 23 rows. First row is the header (CSV).

Questions? Write to us: [keegan@themarkup.org](mailto:keegan@themarkup.org) and [alfred@themarkup.org](mailto:alfred@themarkup.org)

