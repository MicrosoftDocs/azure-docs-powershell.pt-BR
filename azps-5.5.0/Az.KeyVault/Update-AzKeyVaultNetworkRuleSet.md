---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113059"
---
# <span data-ttu-id="25cef-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="25cef-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="25cef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25cef-102">SYNOPSIS</span></span>
<span data-ttu-id="25cef-103">Atualiza o conjunto de regras de rede em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="25cef-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="25cef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25cef-104">SYNTAX</span></span>

### <span data-ttu-id="25cef-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25cef-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25cef-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25cef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="25cef-108">DESCRIPTION</span></span>
<span data-ttu-id="25cef-109">O **comando Update-AzKeyVaultNetworkRuleSet** atualiza as regras de rede em vigor no cofre de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="25cef-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="25cef-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25cef-110">EXAMPLES</span></span>

### <span data-ttu-id="25cef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25cef-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
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
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="25cef-112">Esse comando atualiza o ruleset de rede no cofre chamado "myVault" para o intervalo IP especificado e a rede virtual, permitindo ignorar a regra de rede para os serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="25cef-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="25cef-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25cef-113">Example 2</span></span>

<span data-ttu-id="25cef-114">Atualiza o conjunto de regras de rede em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="25cef-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="25cef-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="25cef-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="25cef-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25cef-116">PARAMETERS</span></span>

### <span data-ttu-id="25cef-117">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="25cef-117">-Bypass</span></span>
<span data-ttu-id="25cef-118">Especifica o bypass da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="25cef-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cef-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="25cef-119">-DefaultAction</span></span>
<span data-ttu-id="25cef-120">Especifica a ação padrão da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="25cef-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cef-121">-DefaultProfile</span></span>
<span data-ttu-id="25cef-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25cef-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25cef-123">-InputObject</span></span>
<span data-ttu-id="25cef-124">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="25cef-124">KeyVault object</span></span>

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

### <span data-ttu-id="25cef-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="25cef-125">-IpAddressRange</span></span>
<span data-ttu-id="25cef-126">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="25cef-126">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="25cef-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25cef-127">-PassThru</span></span>
<span data-ttu-id="25cef-128">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="25cef-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="25cef-129">Se essa opção for especificada, ela retornará o objeto do cofre de chave atualizado.</span><span class="sxs-lookup"><span data-stu-id="25cef-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="25cef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cef-130">-ResourceGroupName</span></span>
<span data-ttu-id="25cef-131">Especifica o nome do grupo de recursos associado ao cofre de chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="25cef-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="25cef-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-132">-ResourceId</span></span>
<span data-ttu-id="25cef-133">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="25cef-133">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="25cef-134">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="25cef-134">-VaultName</span></span>
<span data-ttu-id="25cef-135">Especifica o nome de um cofre de chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="25cef-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="25cef-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="25cef-137">Especifica identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="25cef-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="25cef-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="25cef-138">-Confirm</span></span>
<span data-ttu-id="25cef-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25cef-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cef-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cef-140">-WhatIf</span></span>
<span data-ttu-id="25cef-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="25cef-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25cef-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25cef-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cef-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cef-143">CommonParameters</span></span>
<span data-ttu-id="25cef-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25cef-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cef-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25cef-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cef-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="25cef-146">INPUTS</span></span>

### <span data-ttu-id="25cef-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="25cef-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="25cef-148">System.String</span><span class="sxs-lookup"><span data-stu-id="25cef-148">System.String</span></span>

### <span data-ttu-id="25cef-149">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="25cef-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="25cef-150">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="25cef-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="25cef-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="25cef-151">OUTPUTS</span></span>

### <span data-ttu-id="25cef-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="25cef-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="25cef-153">Notas</span><span class="sxs-lookup"><span data-stu-id="25cef-153">NOTES</span></span>

## <span data-ttu-id="25cef-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25cef-154">RELATED LINKS</span></span>
