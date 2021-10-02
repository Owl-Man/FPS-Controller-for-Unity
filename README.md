# FPS (Frame Per Second) Controller for Unity

By moving the **FPS controller.cs** script to the folder with your other scripts, you can limit the frame rate using the inspector in the Unity
(changing the **FPS** integer variable) or by calling the **SetFps** method. Also, through the inspector (changing the **isVSyncActive** bool variable) or by calling the **DisableVSync/EnableVSync** method, you can turn off and turn on VSync (Vertical Sync). All these methods are in the **FPS Controller** class, which can be accessed using a singleton.

Example:

    using UnityEngine;
    
    public class Test : MonoBehaviour
    {
        private FPSController FPSCntrl;
        
        private void Start() 
        {
            FPSCntrl = FPSController.instance;
            
            FPSCntrl.DisableVSync();
            FPSCntrl.SetFPS(60);
        }
    }

***FPS Controller script must be located on any object in the scene only once to use its functions***
