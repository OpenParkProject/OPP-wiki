# 🛠️ Admin User Guide

The **Admin Dashboard** empowers system administrators to configure zones, manage user accounts, and maintain smart parking infrastructure.

Admins play a central role in managing roles, zones, totems, and system security.

---

## 👤 Create & Manage User Accounts

Admins can create or manage accounts for:

- ✅ **Controller**
- ✅ **Admin**
#### Admin management:
![Admin](imgs/admin/admin.png)
#### Controller management:
![Controller](imgs/admin/controller.png)

### ➕ Add a New User
1. Press the **Add new user(admin, controller)** button on the below.
2. Fill in the form with the required user information:
3. Select the zone you want to assign the user to (if applicable).
4. Click **Create**
#### Add Admin:
![Add Admin](imgs/admin/add_admin.png)
#### Add Controller:
![Add Controller](imgs/admin/add_controller.png)
> You must have at least one zone available for assignment, otherwise some functions of the unassigned Controller accounts will be unavailable.
---
### 🗝️ Login a User
Click the **Enter** button on the right side of the specified account (the first button) to log in to the specified account.
### ❌ Delete a User
Click the **Delete** button on the right side of the specified account (the second button) to delete the specified account.

---

## ➕ Create New Parking Zones
![Zone](imgs/admin/zone.png)
Define zones for precise parking control:
1. Assign **zone name**
2. Fill in **zone pricing configuration**
![Add Zone](imgs/admin/add_zone.png)
3. Set **location boundaries**
![Draw Zone](imgs/admin/draw_zone.png)
4. Press **Create Zone** to create the zone
> 🗺️ After successful creation, you can view the zone boundaries on the map and set whether the zone is active. Inactive zones will not participate in allocation and cannot be selected by other users or non-users.
![See on Map](imgs/admin/see_on_map.png)
> You can also see all zones on the map by pressing **View all on map**.
![All Zones](imgs/admin/all_zone.png)

---

## 🏧Generate OTP and Install Totem

🔐Admins can generate time-limited OTP (One-Time Password) tokens for:
- Securely install Totem throughout the application and enable other users or non-users to pay on Totem.

### 🏗️ How to Generate OTP and Install Totem:
1. Press **Generate New OTP** if there is no OTP available.
![OTP](imgs/admin/no_otp.png)
2. Copy the generated OTP code
![Generate OTP](imgs/admin/generate_otp.png)
3. Logout and press the **Forgot Password?** on the login page.
4. Enter "0" in the **Email** field to open the OTP install mode.
![Install Mode](imgs/admin/install_mode.png)
5. Enter the OTP code in the **OTP** field.
6. Press **OK**
![Vertify Input](imgs/admin/vertify_otp_input.png)
7. Select position on the map and zone to install Totem.
![install Totem](imgs/admin/install_totem.png)
![install Totem](imgs/admin/install_totem2.png)
> Enable RFID reader will change the way of payment in the application, so you can enable it if you want to use RFID card to pay on Totem.
#### At this time, the login interface changes, indicating that totem has been successfully installed.
![Totem Installed](imgs/admin/login_with_totem.png)
#### Totem can be uninstalled in the OTP install mode. Input "DISABLE" in the **OTP** field and press **OK** to uninstall Totem.
![Uninstall Totem](imgs/admin/set_totem_disable.png)
![Totem Uninstalled](imgs/admin/totem_disabled.png)
> Totem installed or not will change the way of payment in the application.

---



## 🗺️ View All Totems

- See a **real-time map** of all active Totems
### No totem:
![No Totem](imgs/admin/no_totem.png)
### With totem:
![With Totem](imgs/admin/with_totem.png)

---

