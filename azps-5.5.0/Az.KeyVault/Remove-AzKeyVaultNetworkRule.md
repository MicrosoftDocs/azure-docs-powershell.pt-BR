---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116712"
---
# <span data-ttu-id="d175f-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d175f-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="d175f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d175f-102">SYNOPSIS</span></span>
<span data-ttu-id="d175f-103">Remove uma regra de rede de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="d175f-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="d175f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d175f-104">SYNTAX</span></span>

### <span data-ttu-id="d175f-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d175f-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d175f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d175f-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d175f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d175f-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d175f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d175f-108">DESCRIPTION</span></span>
<span data-ttu-id="d175f-109">Remove uma regra de rede de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="d175f-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="d175f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d175f-110">EXAMPLES</span></span>

### <span data-ttu-id="d175f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d175f-111">Example 1</span></span>
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

<span data-ttu-id="d175f-112">Esse comando remove uma regra de rede do cofre especificado, desde que uma regra seja encontrada correspondente ao endereço IP especificado e ao identificador de recurso de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d175f-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="d175f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d175f-113">PARAMETERS</span></span>

### <span data-ttu-id="d175f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d175f-114">-DefaultProfile</span></span>
<span data-ttu-id="d175f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d175f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d175f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d175f-116">-InputObject</span></span>
<span data-ttu-id="d175f-117">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="d175f-117">KeyVault object</span></span>

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

### <span data-ttu-id="d175f-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="d175f-118">-IpAddressRange</span></span>
<span data-ttu-id="d175f-119">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="d175f-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="d175f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d175f-120">-PassThru</span></span>
<span data-ttu-id="d175f-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="d175f-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d175f-122">Se essa opção for especificada, ela retornará o objeto do cofre de chave atualizado.</span><span class="sxs-lookup"><span data-stu-id="d175f-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="d175f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d175f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d175f-124">Especifica o nome do grupo de recursos associado ao cofre de chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="d175f-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="d175f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d175f-125">-ResourceId</span></span>
<span data-ttu-id="d175f-126">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="d175f-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="d175f-127">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="d175f-127">-VaultName</span></span>
<span data-ttu-id="d175f-128">Especifica o nome de um cofre de chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="d175f-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="d175f-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d175f-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d175f-130">Especifica identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="d175f-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="d175f-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d175f-131">-Confirm</span></span>
<span data-ttu-id="d175f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d175f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d175f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d175f-133">-WhatIf</span></span>
<span data-ttu-id="d175f-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d175f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d175f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d175f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d175f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d175f-136">CommonParameters</span></span>
<span data-ttu-id="d175f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d175f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d175f-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d175f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d175f-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d175f-139">INPUTS</span></span>

### <span data-ttu-id="d175f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d175f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d175f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d175f-141">System.String</span></span>

## <span data-ttu-id="d175f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="d175f-142">OUTPUTS</span></span>

### <span data-ttu-id="d175f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d175f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d175f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="d175f-144">NOTES</span></span>

## <span data-ttu-id="d175f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d175f-145">RELATED LINKS</span></span>
