# main-character
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class MainCharacter : MonoBehaviour
{
    public Camera MainCamera;
    private Vector3 lastMousePosition;
    private Vector3 newAngle = new Vector3(0, 0, 0);
    int topx,topz;
    int lenthx,lenthz;

    void Update()
    {
        //前に移動します
        if (Input.GetKey(KeyCode.W))
        {
            transform.position += new Vector3(0, 0, 6 * Time.deltaTime);
        }
        //後に移動します
        if (Input.GetKey(KeyCode.X))
        {
            transform.position += new Vector3(0, 0, -6 * Time.deltaTime);
        }
        //右に移動します
        if (Input.GetKey(KeyCode.D))
        {
            transform.position += new Vector3(6 * Time.deltaTime, 0, 0);
        }
        //左に移動します
        if (Input.GetKey(KeyCode.A))
        {
            transform.position += new Vector3(-6 * Time.deltaTime, 0, 0);
        }
        //上に移動します
        if (Input.GetKey(KeyCode.S))
        {
            transform.position += new Vector3(0, 6 * Time.deltaTime, 0);
        }

    }
}
