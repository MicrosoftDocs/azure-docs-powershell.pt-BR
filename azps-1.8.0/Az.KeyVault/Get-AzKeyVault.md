---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 795840d7580d1e7dabb15cf3211ef16d0ccfb7b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770666"
---
# <span data-ttu-id="a9ed1-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="a9ed1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ed1-103">Obtém cofres de chave.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-103">Gets key vaults.</span></span>

## <span data-ttu-id="a9ed1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9ed1-104">SYNTAX</span></span>

### <span data-ttu-id="a9ed1-105">GetVaultByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9ed1-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ed1-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ed1-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="a9ed1-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ed1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9ed1-108">DESCRIPTION</span></span>
<span data-ttu-id="a9ed1-109">O cmdlet **Get-AzKeyVault** Obtém informações sobre os cofres de chaves em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="a9ed1-110">Você pode exibir todas as instâncias de cofre de chaves em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="a9ed1-111">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único cofre de chaves, você deve fazê-lo para obter melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="a9ed1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9ed1-112">EXAMPLES</span></span>

### <span data-ttu-id="a9ed1-113">Exemplo 1: obter todos os cofres de chaves na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a9ed1-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="a9ed1-114">Este comando obtém todos os cofres de chaves na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="a9ed1-115">Exemplo 2: obter um cofre de chaves específico</span><span class="sxs-lookup"><span data-stu-id="a9ed1-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
```

<span data-ttu-id="a9ed1-116">Este comando obtém o cofre de chaves chamado myvault na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="a9ed1-117">Exemplo 3: obter cofres de chaves em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a9ed1-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="a9ed1-118">Esse comando obtém todos os cofres de chaves do grupo de recursos chamado ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="a9ed1-119">Exemplo 4: obter todos os cofres de chaves excluídos na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a9ed1-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="a9ed1-120">Este comando obtém todos os cofres de chaves excluídos na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="a9ed1-121">Exemplo 5: obter um cofre de chaves excluído</span><span class="sxs-lookup"><span data-stu-id="a9ed1-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="a9ed1-122">Este comando obtém as informações excluídas do cofre de chaves chamadas myvault4 na sua assinatura atual e na região da região oeste.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="a9ed1-123">Exemplo 6: obter cofres de chaves usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="a9ed1-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="a9ed1-124">Esse comando obtém todos os cofres de chaves na assinatura que começam com "myvault".</span><span class="sxs-lookup"><span data-stu-id="a9ed1-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="a9ed1-125">OS</span><span class="sxs-lookup"><span data-stu-id="a9ed1-125">PARAMETERS</span></span>

### <span data-ttu-id="a9ed1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ed1-126">-DefaultProfile</span></span>
<span data-ttu-id="a9ed1-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9ed1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ed1-128">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="a9ed1-128">-InRemovedState</span></span>
<span data-ttu-id="a9ed1-129">Especifica se os cofres excluídos anteriormente devem ser mostrados na saída.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ed1-130">-Local</span><span class="sxs-lookup"><span data-stu-id="a9ed1-130">-Location</span></span>
<span data-ttu-id="a9ed1-131">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ed1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ed1-132">-ResourceGroupName</span></span>
<span data-ttu-id="a9ed1-133">Especifica o nome do grupo de recursos associado ao cofre de chaves ou a cofres de chaves sendo consultados.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a9ed1-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="a9ed1-134">-Tag</span></span>
<span data-ttu-id="a9ed1-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a9ed1-136">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a9ed1-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ed1-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a9ed1-137">-VaultName</span></span>
<span data-ttu-id="a9ed1-138">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a9ed1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ed1-139">CommonParameters</span></span>
<span data-ttu-id="a9ed1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ed1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ed1-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9ed1-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ed1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9ed1-142">INPUTS</span></span>

### <span data-ttu-id="a9ed1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ed1-143">System.String</span></span>

### <span data-ttu-id="a9ed1-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9ed1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a9ed1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9ed1-145">OUTPUTS</span></span>

### <span data-ttu-id="a9ed1-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a9ed1-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a9ed1-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="a9ed1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="a9ed1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9ed1-149">NOTES</span></span>

## <span data-ttu-id="a9ed1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9ed1-150">RELATED LINKS</span></span>

[<span data-ttu-id="a9ed1-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="a9ed1-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9ed1-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
