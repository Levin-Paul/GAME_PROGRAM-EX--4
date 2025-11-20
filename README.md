# GAME_PROGRAM-EX--4
# AIM :
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.
# PROCEDURE :
# 1.Attach the Rifle to the Character
Import the Rifle Skeletal Mesh into Unreal Engine. Open your Character Blueprint (e.g., BP_ThirdPersonCharacter). In the Components tab: Add a Skeletal Mesh or Static Mesh component (name it Rifle). Set its Skeletal Mesh to your rifle asset.

# 2.Attach the Rifle to a socket on the character’s skeleton

In the Rifle component, set the Parent Socket to something like hand_r (right hand socket).




manually attach in Event Graph:
Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");

# 3. Add Aiming Mechanism
Create a Boolean variable called IsAiming. Set up Input in Project Settings: Go to Edit > Project Settings > Input. Add an Action Mapping named Aim (e.g., Right Mouse Button).

# 4. Adjust Camera When Aiming
Add a Camera Boom and Follow Camera.


In Event Graph:

When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.


# OUTPUT :

<img width="1033" height="826" alt="image" src="https://github.com/user-attachments/assets/13b5799c-4782-4544-aef8-9cc85aadd85a" />


<img width="1139" height="855" alt="image" src="https://github.com/user-attachments/assets/72519443-3db8-4bc9-ad58-ad90da7025f4" />


# RESULT :

Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.
