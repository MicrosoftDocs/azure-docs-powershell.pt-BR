---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: 6949de15168043e9ede9e8a023f6f5fcec333557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885449"
---
# <span data-ttu-id="312fe-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="312fe-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="312fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312fe-102">SYNOPSIS</span></span>
<span data-ttu-id="312fe-103">Remove uma regra de rede de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="312fe-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="312fe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="312fe-104">SYNTAX</span></span>

### <span data-ttu-id="312fe-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="312fe-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="312fe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="312fe-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="312fe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="312fe-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="312fe-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="312fe-108">DESCRIPTION</span></span>
<span data-ttu-id="312fe-109">Remove uma regra de rede de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="312fe-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="312fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="312fe-110">EXAMPLES</span></span>

### <span data-ttu-id="312fe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="312fe-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="312fe-112">Este comando remove uma regra de rede do cofre especificado, desde que uma regra seja encontrada correspondendo ao endereço IP especificado e ao identificador de recurso de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="312fe-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="312fe-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="312fe-113">PARAMETERS</span></span>

### <span data-ttu-id="312fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312fe-114">-DefaultProfile</span></span>
<span data-ttu-id="312fe-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="312fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="312fe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="312fe-116">-InputObject</span></span>
<span data-ttu-id="312fe-117">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="312fe-117">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="312fe-118">-IpAddressRange</span></span>
<span data-ttu-id="312fe-119">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="312fe-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="312fe-120">-PassThru</span></span>
<span data-ttu-id="312fe-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="312fe-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="312fe-122">Se essa opção for especificada, ela retornará o objeto do cofre de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="312fe-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="312fe-124">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="312fe-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="312fe-125">-ResourceId</span></span>
<span data-ttu-id="312fe-126">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="312fe-126">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="312fe-127">-VaultName</span></span>
<span data-ttu-id="312fe-128">Especifica o nome de um cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="312fe-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="312fe-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="312fe-130">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="312fe-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="312fe-131">-Confirm</span></span>
<span data-ttu-id="312fe-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="312fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="312fe-133">-WhatIf</span></span>
<span data-ttu-id="312fe-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="312fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="312fe-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="312fe-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312fe-136">CommonParameters</span></span>
<span data-ttu-id="312fe-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="312fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312fe-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="312fe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312fe-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="312fe-139">INPUTS</span></span>

### <span data-ttu-id="312fe-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="312fe-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="312fe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="312fe-141">System.String</span></span>

## <span data-ttu-id="312fe-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="312fe-142">OUTPUTS</span></span>

### <span data-ttu-id="312fe-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="312fe-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="312fe-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="312fe-144">NOTES</span></span>

## <span data-ttu-id="312fe-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="312fe-145">RELATED LINKS</span></span>
