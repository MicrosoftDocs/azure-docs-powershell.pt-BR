---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: dda32611087046a9e31f9e2d00edc8f648180fe5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886224"
---
# <span data-ttu-id="d27ee-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d27ee-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="d27ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d27ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d27ee-103">Adiciona uma regra destinada a restringir o acesso a um cofre de chaves com base no endereço da Internet do cliente.</span><span class="sxs-lookup"><span data-stu-id="d27ee-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="d27ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d27ee-104">SYNTAX</span></span>

### <span data-ttu-id="d27ee-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d27ee-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d27ee-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d27ee-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d27ee-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d27ee-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d27ee-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d27ee-108">DESCRIPTION</span></span>
<span data-ttu-id="d27ee-109">O cmdlet **Add-AzKeyVaultNetworkRule** concede ou restringe o acesso a um cofre de chaves para um conjunto de chamador designado por seus endereços IP ou pela rede virtual à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="d27ee-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="d27ee-110">A regra tem o potencial de restringir o acesso a outros usuários, aplicativos ou grupos de segurança que tenham sido concedidas permissões por meio da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="d27ee-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="d27ee-111">Observe que qualquer intervalo IP dentro `10.0.0.0-10.255.255.255` (endereços IP particulares) não pode ser usado para adicionar regras de rede.</span><span class="sxs-lookup"><span data-stu-id="d27ee-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="d27ee-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d27ee-112">EXAMPLES</span></span>

### <span data-ttu-id="d27ee-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d27ee-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
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


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="d27ee-114">Este comando adiciona uma regra de rede ao cofre especificado, permitindo o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="d27ee-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="d27ee-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d27ee-115">PARAMETERS</span></span>

### <span data-ttu-id="d27ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27ee-116">-DefaultProfile</span></span>
<span data-ttu-id="d27ee-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d27ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27ee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d27ee-118">-InputObject</span></span>
<span data-ttu-id="d27ee-119">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="d27ee-119">KeyVault object</span></span>

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

### <span data-ttu-id="d27ee-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="d27ee-120">-IpAddressRange</span></span>
<span data-ttu-id="d27ee-121">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="d27ee-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="d27ee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d27ee-122">-PassThru</span></span>
<span data-ttu-id="d27ee-123">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="d27ee-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d27ee-124">Se essa opção for especificada, ela retornará o objeto do cofre de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="d27ee-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="d27ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="d27ee-126">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="d27ee-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="d27ee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d27ee-127">-ResourceId</span></span>
<span data-ttu-id="d27ee-128">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="d27ee-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="d27ee-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d27ee-129">-VaultName</span></span>
<span data-ttu-id="d27ee-130">Especifica o nome de um cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="d27ee-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="d27ee-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d27ee-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d27ee-132">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="d27ee-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="d27ee-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d27ee-133">-Confirm</span></span>
<span data-ttu-id="d27ee-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d27ee-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d27ee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d27ee-135">-WhatIf</span></span>
<span data-ttu-id="d27ee-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d27ee-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27ee-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d27ee-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d27ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27ee-138">CommonParameters</span></span>
<span data-ttu-id="d27ee-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d27ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27ee-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d27ee-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27ee-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d27ee-141">INPUTS</span></span>

### <span data-ttu-id="d27ee-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d27ee-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d27ee-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d27ee-143">System.String</span></span>

## <span data-ttu-id="d27ee-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d27ee-144">OUTPUTS</span></span>

### <span data-ttu-id="d27ee-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d27ee-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d27ee-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="d27ee-146">NOTES</span></span>

## <span data-ttu-id="d27ee-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d27ee-147">RELATED LINKS</span></span>
