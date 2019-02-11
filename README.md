# Complete PNG encoding and decoding for Unity engine.

TODO:
- Replace use of Color[] with NativeArray<byte>
- PNG.READ creating Texture2D in every useful TextureFormat (infered from file)
- PNG.READ with target TextureFormat argument
- PNG.READ with target width and height arguemnts
- Improve READ/WRITE speeds

HOW TO USE:
```C#
using System.Threading.Tasks;
using UnityEngine;
using using Pngcs.Unity;
public class PngcsTest : MonoBehaviour
{
    async void Awake ()
    {
        // THIS IS HOW YOU READ:
        Texture2D texture = await PNG.READ( @"D:/input.png" );

        // THIS IS HOW YOU WRITE:
        PNG.WRITE( texture , @"D:/output.png" );
        
        //remember to always release memory when texture is not needed anymore:
        Destroy( texture );
    }
}
```
