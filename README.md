# ReskinGuard Unity Package

ReskinGuard is a Unity package designed to protect your Unity project from being reskinned or cloned. It helps prevent unauthorized use of your game's codebase by detecting package name changes and redirecting users to the original version on the appropriate app store if a cloned version is detected.

## Integration Steps:

To integrate ReskinGuard into your Unity project, follow the steps below:

### 1. Add the ReskinGuard Package:

You can add the ReskinGuard package to your Unity project by either importing the `ReskinGuard.unitypackage`

1. **Download the Package**:
   - Download the `ReskinGuard.unitypackage` file.

2. **Open Your Unity Project**:
   - Launch the Unity Editor and open the Unity project you want to add ReskinGuard to.

3. **Import the Package**:
   - Click on the `Assets` menu in the Unity Editor then select `Import Package` > `Custom Package`.

4. **Locate and Choose the ReskinGuard.unitypackage File**:
   - Browse your file system and select the `ReskinGuard.unitypackage` file you downloaded.


### 2. Add the Code to the First Scene:

In the first scene of your Unity project, open the script attached to your main game object and add the following code:

```csharp
  void OnApplicationFocus(bool hasFocus) {
    	if (hasFocus) {
      		string EXPN = "Encoded Here"; // Replace this with the actual encoded value obtained from the console during first run of the game.
      		gameObject.AddComponent<ReskinGurad>();
      		ReskinGurad Chk = GetComponent<ReskinGurad>();
      		Chk.ChkPN(EXPN);
    	}
  }
```

### 3. Encode the Value:
Before Publishing the game, make sure to replace "Encoded Here" with the actual encoded value that you obtained during the initial setup. This encoded value will be used by ReskinGuard to verify the authenticity of the app.

### 4. Build and Run:
Build your Unity application and run it. ReskinGuard will now be protecting your game from unauthorized reskinning and tampering.

## Game Redirection:
If someone attempts to clone your game and publish it, ReskinGuard will automatically detect the package name change and redirect users back to the original version on the appropriate app store. This ensures that users only interact with the legitimate version of your game.

By integrating ReskinGuard into your Unity project, you enhance the security of your game, protect your intellectual property, and maintain user trust in the authenticity of your application.


To get the ReskinGuard plugin for Android Studio, please visit : [ReskinGuard For Android Studio](https://github.com/Mohammedcha/ReskinGuard)


