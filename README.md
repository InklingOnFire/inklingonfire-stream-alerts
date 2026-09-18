# Stream Alerts for InklingOnFire

inkling-on-fire-alerts is a [NodeCG](http://github.com/nodecg/nodecg) bundle.
It works with NodeCG versions which satisfy this [semver](https://docs.npmjs.com/getting-started/semantic-versioning) range: `^2.0.0`
You will need to have an appropriate version of NodeCG installed to use it.

## Disclaimers
This is a stream alerts project by me (InklingOnFire) for my own streams.
Most of the resources have been heavily inspired by Splatoon Raiders.
This project is not affiliated with Nintendo in any way, shape or form.

This project is **unfinished** and may contain a lot of bugs. It's also my very first web project and I'm open to suggestions for improvement.

## Contributing
You may contribute to this project by forking it and creating a pull request.

## Installation and Usage
### What you need:
- [NodeCG](http://github.com/nodecg/nodecg) installed.
- A Twitch application

### Installing NodeCG and the bundle
Refer to the [NodeCG Installation Guide](https://www.nodecg.dev/docs/installing).

To install this bundle, use

    nodecg install inklingonfire/inklingonfire-stream-alerts

in a CLI shell of your choice.

### Twitch Application
> [!NOTE]
> 
> You will need a Twitch application to be able to listen to EventSub events (subs, bits, etc.)

1. Head over to the Twitch Developer Console.
2. Create an application. You can name it whatever you want.
3. Set the redirect URLs to:
    - `http://localhost:9090`
    - `http://localhost:9090/inkling-on-fire-alerts/extension/auth/auth`
4. Save the changes made to your Twitch Application.
5. Insert the generated Client ID into "Settings" -> "Twitch" -> "Client ID".
6. Generate a new Client Secret and insert it into "Settings" -> "Twitch" -> "Client Secret".
> [!DANGER]
> 
> Your Client secret is, well, supposed to be secret. Don't leak it **UNDER ANY CIRCUMSTANCES.**
7. Log in via the 'Log In' button. Your access token and refresh token will be saved in the `userAuth` replicant.
> [!DANGER]
> 
> The access and refresh token must also not be leaked **UNDER ANY CIRCUMSTANCES.**

EventSub will activate and subscribe to events automatically.

## Starting the bundle
Use

    nodecg start

to start NodeCG. By default, NodeCG launches and is accessible at `http://localhost:9090`.

> [!IMPORTANT]
>
> If you ever plan to change that, remember to change the redirect URLs as well!

