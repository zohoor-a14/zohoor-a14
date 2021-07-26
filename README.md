using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class NewBehaviourScript : MonoBehaviour
{
    private int CurrentHealth;
    private int MaximumHealth;
}
//return maximun health
public int GetMaximumHealth()
{
    return MaximumHealth;
}
//return current health
public int GetCurrentHealth()
{
    return CurrentHealth;
}
//add current  health
public void AddHealth(int Amount)
{
    CurrentHealth += Amount;
    CurrentHealth = Mathf.Clamp(CurrentHealth, 0, MaximumHealth);

}
//remove from current health
public void RemoveHealth(int Amount)
{
    CurrentHealth -= Amount;
    CurrentHealth = Mathf.Clamp(CurrentHealth, 0, MaximumHealth);

}
//fill up health
public void FullHealth()
{
    CurrentHealth = MaximumHealth;
}

