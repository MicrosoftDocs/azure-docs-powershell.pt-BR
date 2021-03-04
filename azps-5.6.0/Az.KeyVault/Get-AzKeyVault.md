---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 84148d675b5c6bc43a883ecd5c419b5019de49d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893277"
---
# <span data-ttu-id="44b0b-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="44b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="44b0b-103">Obtém cofres chave.</span><span class="sxs-lookup"><span data-stu-id="44b0b-103">Gets key vaults.</span></span>

## <span data-ttu-id="44b0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44b0b-104">SYNTAX</span></span>

### <span data-ttu-id="44b0b-105">GetVaultByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44b0b-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b0b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b0b-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="44b0b-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44b0b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44b0b-108">DESCRIPTION</span></span>
<span data-ttu-id="44b0b-109">O cmdlet **Get-AzKeyVault** obtém informações sobre os cofres de chaves em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="44b0b-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="44b0b-110">Você pode exibir todas as instâncias de cofres-chave em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.</span><span class="sxs-lookup"><span data-stu-id="44b0b-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="44b0b-111">Observe que, embora a especificação do grupo de recursos seja opcional para este cmdlet quando você obter um único cofre de chaves, você deve fazer isso para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="44b0b-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="44b0b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44b0b-112">EXAMPLES</span></span>

### <span data-ttu-id="44b0b-113">Exemplo 1: Obter todos os cofres de chaves em sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="44b0b-113">Example 1: Get all key vaults in your current subscription</span></span>
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

<span data-ttu-id="44b0b-114">Esse comando obtém todos os cofres de chave em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="44b0b-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="44b0b-115">Exemplo 2: Obter um cofre de chaves específico</span><span class="sxs-lookup"><span data-stu-id="44b0b-115">Example 2: Get a specific key vault</span></span>
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

<span data-ttu-id="44b0b-116">Este comando obtém o cofre de chaves chamado myvault em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="44b0b-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="44b0b-117">Exemplo 3: Obter cofres chave em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44b0b-117">Example 3: Get key vaults in a resource group</span></span>
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

<span data-ttu-id="44b0b-118">Este comando obtém todos os cofres de chave no grupo de recursos chamado ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="44b0b-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="44b0b-119">Exemplo 4: Obter todos os cofres de chaves excluídos em sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="44b0b-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
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

<span data-ttu-id="44b0b-120">Este comando obtém todos os cofres de chave excluídos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="44b0b-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="44b0b-121">Exemplo 5: Obter um cofre de chaves excluído</span><span class="sxs-lookup"><span data-stu-id="44b0b-121">Example 5: Get a deleted key vault</span></span>
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

<span data-ttu-id="44b0b-122">Este comando obtém as informações do cofre de chaves excluídas denominadas myvault4 em sua assinatura atual e na região de westus.</span><span class="sxs-lookup"><span data-stu-id="44b0b-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="44b0b-123">Exemplo 6: Obter cofres de chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="44b0b-123">Example 6: Get key vaults using filtering</span></span>
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

<span data-ttu-id="44b0b-124">Este comando obtém todos os cofres de chave na assinatura que começam com "myvault".</span><span class="sxs-lookup"><span data-stu-id="44b0b-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="44b0b-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44b0b-125">PARAMETERS</span></span>

### <span data-ttu-id="44b0b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b0b-126">-DefaultProfile</span></span>
<span data-ttu-id="44b0b-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="44b0b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44b0b-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="44b0b-128">-InRemovedState</span></span>
<span data-ttu-id="44b0b-129">Especifica se os cofres excluídos anteriormente serão indicados na saída.</span><span class="sxs-lookup"><span data-stu-id="44b0b-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="44b0b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="44b0b-130">-Location</span></span>
<span data-ttu-id="44b0b-131">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="44b0b-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="44b0b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b0b-132">-ResourceGroupName</span></span>
<span data-ttu-id="44b0b-133">Especifica o nome do grupo de recursos associado ao cofre de chaves ou aos cofres chave que estão sendo consultados.</span><span class="sxs-lookup"><span data-stu-id="44b0b-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="44b0b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="44b0b-134">-Tag</span></span>
<span data-ttu-id="44b0b-135">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="44b0b-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="44b0b-136">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="44b0b-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="44b0b-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="44b0b-137">-VaultName</span></span>
<span data-ttu-id="44b0b-138">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="44b0b-138">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="44b0b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b0b-139">CommonParameters</span></span>
<span data-ttu-id="44b0b-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b0b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b0b-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44b0b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b0b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44b0b-142">INPUTS</span></span>

### <span data-ttu-id="44b0b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="44b0b-143">System.String</span></span>

### <span data-ttu-id="44b0b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="44b0b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="44b0b-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44b0b-145">OUTPUTS</span></span>

### <span data-ttu-id="44b0b-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="44b0b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="44b0b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="44b0b-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="44b0b-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="44b0b-149">NOTES</span></span>

## <span data-ttu-id="44b0b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44b0b-150">RELATED LINKS</span></span>

[<span data-ttu-id="44b0b-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="44b0b-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="44b0b-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
