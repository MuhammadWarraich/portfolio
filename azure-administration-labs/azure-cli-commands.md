# Azure CLI Commands

## Login to Azure

```bash
az login
```

---

## List Resource Groups

```bash
az group list
```

---

## Create Resource Group

```bash
az group create --name MyResourceGroup --location eastus
```

---

## List Virtual Machines

```bash
az vm list -o table
```

---

## Start Virtual Machine

```bash
az vm start --name MyVM --resource-group MyResourceGroup
```

---

## Stop Virtual Machine

```bash
az vm stop --name MyVM --resource-group MyResourceGroup
```

---

## Check Public IP Addresses

```bash
az network public-ip list -o table
```

---

## List NSGs

```bash
az network nsg list -o table
```

---

## List Storage Accounts

```bash
az storage account list -o table
```

---

## List Backup Vaults

```bash
az backup vault list
```

---

# Note

Example commands are for educational and lab purposes only. Sensitive production information has been removed.
