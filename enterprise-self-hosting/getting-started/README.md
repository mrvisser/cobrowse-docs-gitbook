# Running your instance

Once your self-hosted instance is up and running, there are a few steps to bootstrap the account and configure our SDKs to use your private instance.

## Register an account

Once your instance is up and running, you will need to register yourself an account. Head to [https://&lt;your instance domain&gt;/register](https://cobrowse.io/register) to setup your account. 

You may register multiple accounts in your instance if you would like. Some customers register accounts for dev, test, staging, etc. 

{% hint style="info" %}
If you are using the Email "magic link" sign-in flow, but do not have a mail server set up and have disabled our default mail provider, then please retrieve the "magic link" used to sign-in directly via the application logs of the cobrowe-api container. 
{% endhint %}

## Setting API location in the SDKs

You will need to set the API location when integrating the SDKs in order to point them at your private instance.

{% hint style="info" %}
When specifying the API, please do not use a trailing slash. 
{% endhint %}

{% tabs %}
{% tab title="Web" %}
```javascript
CobrowseIO.api = "https://cobrowse.example.com";
```
{% endtab %}

{% tab title="iOS" %}
```objectivec
CobrowseIO.instance.api = @"https://cobrowse.example.com";
```
{% endtab %}

{% tab title="Android" %}
```java
CobrowseIO.instance().api("https://cobrowse.example.com");
```
{% endtab %}
{% endtabs %}

## Useful resources

Now your instance is up an running, you should review the documentation below to fine tune your deployment.

{% page-ref page="adding-a-superuser.md" %}

{% page-ref page="limiting-account-creation.md" %}

{% page-ref page="configuring-smtp.md" %}

{% page-ref page="management.md" %}

