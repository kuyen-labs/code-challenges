# Fuul Frontend Code Challenge

Fuul provides a React components SDK for clients to implement on their website. 

With the idea to increase the number of active referrers, once a user performs a certain event on the app, crypto projects insert a modal inciting the user to refer others and earn commissions.

The task is to build a generic website (or blank) where users connect their wallet, perform the action and then trigger this modal. The modal component should be imported from a local NPM package.

#### The SDK package should include:
* 1 exported class named "Fuul" which exposes only 2 methods: `init` and `showReferralModal`
* The `init` takes only the `apiKey` argument, gets the project information from a mocked API call and exposes it to all methods.

#### The website should include:
* A connect wallet button. You can use any type of wallet or provider.
* A "perform action" button (let's call it mint, trade, deposit, or any onchain action that you want). This button should prompt the user to sign a message using their wallet and then trigger the referral modal.

#### The modal should include:
* The user's tracking link. The tracking link must be something like `https://app.fuul.xyz/?referrer={connectedAddress}` using the address that is connected to the site.
* The necessary project information from the mocked api call. Feel free to add the information that you think is relevant to show the user.

#### The code should:
* Be written as production-ready code. You will write production code.
* Be easy to grow and easy to add new functionality.
* The code should be written in Typescript.
* If possible, try to use standard html and/or plain javascript for the modal component.