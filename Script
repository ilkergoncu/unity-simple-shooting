using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Shooting : MonoBehaviour
{
    // Start is called before the first frame update

    public Transform firePoint;
    
    // Firepoint is the location where will be the bullet instantiated
    
    
    [SerializeField] private GameObject bullet;
   

    public float bulletForce = 50f;

    private float FireRate = 3f;

    private float lastTimefired;


    void Start()
    {
      
    }

    // Update is called once per frame
    
    void Update()
    {
        
        if (Input.GetKeyDown("space"))
        {
       
        //Here we check if we are shooting according to our fire rate
         if (Time.time - lastTimefired > 1 / FireRate)
       
        {
            lastTimefired = Time.time;

            Shoot();
        }
        
        }
       
    }

    void Shoot()
    {

       

        {
            GameObject b = Instantiate(bullet, firePoint.position, firePoint.rotation);

            b.gameObject.tag = "Bullet";

            Rigidbody rb = b.GetComponent<Rigidbody>();

            rb.AddForce(firePoint.forward * bulletForce, ForceMode.Impulse);


        }
        
    }

}
