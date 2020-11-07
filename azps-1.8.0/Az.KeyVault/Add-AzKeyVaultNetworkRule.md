---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: fd93a933b394fc8729186c7ea78c737123149bf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770674"
---
# <span data-ttu-id="f3f63-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3f63-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="f3f63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3f63-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f63-103">Adiciona uma regra para restringir o acesso a um cofre de chaves baseado no endereço de Internet do cliente.</span><span class="sxs-lookup"><span data-stu-id="f3f63-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="f3f63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3f63-104">SYNTAX</span></span>

### <span data-ttu-id="f3f63-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3f63-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3f63-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3f63-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3f63-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f63-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3f63-108">DESCRIPTION</span></span>
<span data-ttu-id="f3f63-109">O cmdlet **Add-AzKeyVaultNetworkRule** concede ou restringe o acesso a um cofre de chaves a um conjunto de chamadas designado por seus endereços IP ou à rede virtual à qual eles pertencem.</span><span class="sxs-lookup"><span data-stu-id="f3f63-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="f3f63-110">A regra tem o potencial de restringir o acesso para outros usuários, aplicativos ou grupos de segurança que receberam permissões por meio da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3f63-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="f3f63-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3f63-111">EXAMPLES</span></span>

### <span data-ttu-id="f3f63-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3f63-112">Example 1</span></span>
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

<span data-ttu-id="f3f63-113">Esse comando adiciona uma regra de rede ao cofre especificado, permitindo o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="f3f63-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="f3f63-114">OS</span><span class="sxs-lookup"><span data-stu-id="f3f63-114">PARAMETERS</span></span>

### <span data-ttu-id="f3f63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f63-115">-DefaultProfile</span></span>
<span data-ttu-id="f3f63-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3f63-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3f63-117">-InputObject</span></span>
<span data-ttu-id="f3f63-118">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="f3f63-118">KeyVault object</span></span>

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

### <span data-ttu-id="f3f63-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="f3f63-119">-IpAddressRange</span></span>
<span data-ttu-id="f3f63-120">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="f3f63-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="f3f63-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3f63-121">-PassThru</span></span>
<span data-ttu-id="f3f63-122">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f3f63-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f3f63-123">Se essa opção for especificada, ela retornará o objeto do cofre de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="f3f63-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="f3f63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f63-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3f63-125">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="f3f63-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f3f63-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f63-126">-ResourceId</span></span>
<span data-ttu-id="f3f63-127">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="f3f63-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="f3f63-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="f3f63-128">-VaultName</span></span>
<span data-ttu-id="f3f63-129">Especifica o nome de um cofre da chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="f3f63-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f3f63-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f63-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f3f63-131">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="f3f63-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="f3f63-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3f63-132">-Confirm</span></span>
<span data-ttu-id="f3f63-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3f63-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f63-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f63-134">-WhatIf</span></span>
<span data-ttu-id="f3f63-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3f63-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f63-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3f63-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f63-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f63-137">CommonParameters</span></span>
<span data-ttu-id="f3f63-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f63-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f63-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f63-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f63-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3f63-140">INPUTS</span></span>

### <span data-ttu-id="f3f63-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3f63-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f3f63-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f3f63-142">System.String</span></span>

## <span data-ttu-id="f3f63-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3f63-143">OUTPUTS</span></span>

### <span data-ttu-id="f3f63-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3f63-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f3f63-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3f63-145">NOTES</span></span>

## <span data-ttu-id="f3f63-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3f63-146">RELATED LINKS</span></span>
