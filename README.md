3DSView
=======

Self-contained UI component to process banking 3DS (MasterCard Secure Code / Verified By Visa) payment 
authorizations in Android apps.

It handles the complete process from redirecting user to an ACS banking server, displaying web interface for payment 
authorization and "cathcing" authorization results and parameters.

Component can be used in activity or fragment instead of WebView (actually it contains an embedded WebView) or in any
part of the master view. Just add it to your layout, set paramenets and authorization callbacks and invoike 
the performAuthorization(...) method.



# Quick Usage

- Build your own or download precompiled 3dsview.jar from releases section and put it to the libs folder of your app project.
- Add eu.livotov.labs.android.ddds.DDDSView to your layout
- Set auhtorization listener to handle authorization events
- Call dddsView.authorize(...) to begin authorization process

Once user completes the authorization, your callback method will be called with the 3DS response data (MD and PaRes), 
ready to be passed to your credit card processing gateway for payment finalization.