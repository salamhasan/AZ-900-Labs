
# 🔐 Exercise - Configure a Resource Lock in Azure

## ✅ What I Did
In this exercise, I learned how to use **Azure Resource Locks** to protect resources from accidental deletion or modification. I used a **Storage Account** to test both lock types (`ReadOnly` and `Delete`) and observed their impact.

## 🧪 Steps Completed

### 1. Create a Storage Account
- Created a new resource group
- Provisioned a storage account with:
  - Standard performance
  - Locally redundant storage (LRS)
  - Default region

### 2. Apply a ReadOnly Lock
- Added a lock named `ReadOnlyLock`
- Lock type: `ReadOnly`
- Tried to create a container → ❌ Failed due to lock

### 3. Modify Lock to Delete
- Changed lock type to `Delete`
- Created a container successfully ✅

### 4. Attempt to Delete Storage Account
- Tried to delete the storage account → ❌ Failed due to delete lock

### 5. Remove Lock and Delete Resource
- Removed the delete lock
- Deleted the storage account successfully ✅

## 📘 What I Learned
- **ReadOnly Lock** prevents any changes (create/update/delete)
- **Delete Lock** allows changes but blocks deletion
- Locks override RBAC permissions—even Owners must remove the lock first
- Locks are inherited by all resources within a resource group

## 🛠️ Tools Used
- Azure Portal
- Resource Locks (Settings > Locks)
- Storage Account > Containers
## 📸 Screenshots (Optional)
You can add screenshots here if you captured any during the exercise.

## 🔗 Reference
[https://learn.microsoft.com/en-us/training/modules/describe-azure-management-governance/](https://learn.microsoft.com/en-us/training/modules/describe-features-tools-azure-for-governance-compliance/5-exercise-configure-resource-lock)
# AZ-900-Labs
Microsoft Azure Fundamentals - Exercise
