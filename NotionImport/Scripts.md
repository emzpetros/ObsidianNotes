using System.Collections;  
using System.Collections.Generic;  
using NUnit.Framework;  
using UnityEngine;  
using UnityEngine.TestTools;  
using UnityEngine.SceneManagement;

public class MenuTest  
{  
private GameObject gameManager;  
private OptionsMenu optionsMenu;

```
[SetUp]public void Before(){    gameManager = MonoBehaviour.Instantiate(Resources.Load<GameObject>("Board")) as GameObject;    gameManager.AddComponent<OptionsMenu>();    optionsMenu = gameManager.GetComponent<OptionsMenu>();}/*[Test]public void StartGameTest(){    optionsMenu.StartGame();    Assert.AreEqual("MenuScene",SceneManager.GetActiveScene().name );}*/[Test]public void StartTutorialTest(){    optionsMenu.StartTutorial();    Assert.True(GameObject.Find("Tutorial Screen").activeSelf);}
```

}