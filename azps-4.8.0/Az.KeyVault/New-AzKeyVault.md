---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111736"
---
# <span data-ttu-id="22405-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22405-101">New-AzKeyVault</span></span>

## <span data-ttu-id="22405-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22405-102">SYNOPSIS</span></span>
<span data-ttu-id="22405-103">Cria um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-103">Creates a key vault.</span></span>

## <span data-ttu-id="22405-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22405-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22405-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22405-105">DESCRIPTION</span></span>
<span data-ttu-id="22405-106">O cmdlet **New-AzKeyVault** cria um cofre de chaves no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="22405-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="22405-107">Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="22405-108">Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="22405-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="22405-109">Para obter mais informações, consulte Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="22405-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="22405-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22405-110">EXAMPLES</span></span>

### <span data-ttu-id="22405-111">Exemplo 1: criar um cofre de chaves padrão</span><span class="sxs-lookup"><span data-stu-id="22405-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
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

Tags                             :
```

<span data-ttu-id="22405-112">Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="22405-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="22405-113">O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14.</span><span class="sxs-lookup"><span data-stu-id="22405-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="22405-114">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="22405-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="22405-115">Exemplo 2: criar um cofre de chave Premium</span><span class="sxs-lookup"><span data-stu-id="22405-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
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

Tags                             :
```

<span data-ttu-id="22405-116">Esse comando cria um cofre de chaves, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="22405-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="22405-117">No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.</span><span class="sxs-lookup"><span data-stu-id="22405-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="22405-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="22405-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="22405-119">Criando um cofre de chaves e especifica regras de rede para permitir o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="22405-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="22405-120">Consulte `New-AzKeyVaultNetworkRuleSetObject` para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22405-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="22405-121">OS</span><span class="sxs-lookup"><span data-stu-id="22405-121">PARAMETERS</span></span>

### <span data-ttu-id="22405-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22405-122">-DefaultProfile</span></span>
<span data-ttu-id="22405-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22405-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22405-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="22405-124">-DisableSoftDelete</span></span>
<span data-ttu-id="22405-125">Se especificado, a funcionalidade ' exclusão reversível ' é desativada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="22405-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="22405-126">-EnabledForDeployment</span></span>
<span data-ttu-id="22405-127">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="22405-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="22405-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="22405-129">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="22405-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="22405-131">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="22405-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="22405-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="22405-133">Se especificado, a proteção contra exclusão imediata estará habilitada para este cofre; requer a exclusão reversível para ser habilitada também.</span><span class="sxs-lookup"><span data-stu-id="22405-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="22405-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="22405-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="22405-135">Se especificado, habilita a autorização de ações de dados pelo controle de acesso baseado em função (RBAC) e, em seguida, as políticas de acesso especificadas nas propriedades do cofre serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="22405-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="22405-136">Observe que as ações de gerenciamento sempre são autorizadas com RBAC.</span><span class="sxs-lookup"><span data-stu-id="22405-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="22405-137">-Local</span><span class="sxs-lookup"><span data-stu-id="22405-137">-Location</span></span>
<span data-ttu-id="22405-138">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="22405-139">Use o comando [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="22405-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="22405-140">-Name</span></span>
<span data-ttu-id="22405-141">Especifica o nome do cofre de chaves a ser criado.</span><span class="sxs-lookup"><span data-stu-id="22405-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="22405-142">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="22405-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="22405-143">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="22405-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="22405-144">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="22405-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="22405-145">-NetworkRuleSet</span></span>
<span data-ttu-id="22405-146">Especifica o conjunto de regras de rede do cofre.</span><span class="sxs-lookup"><span data-stu-id="22405-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="22405-147">Ele rege a acessibilidade do cofre de chaves de locais de rede específicos.</span><span class="sxs-lookup"><span data-stu-id="22405-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="22405-148">Criado por `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="22405-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22405-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22405-149">-ResourceGroupName</span></span>
<span data-ttu-id="22405-150">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="22405-151">-Sku</span></span>
<span data-ttu-id="22405-152">Especifica a SKU da instância do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="22405-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="22405-153">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="22405-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-154">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="22405-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="22405-155">Especifica por quanto tempo os recursos excluídos são mantidos e quanto tempo até um cofre ou um objeto no estado excluído pode ser limpo.</span><span class="sxs-lookup"><span data-stu-id="22405-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="22405-156">O padrão é 90 dias.</span><span class="sxs-lookup"><span data-stu-id="22405-156">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22405-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="22405-157">-Tag</span></span>
<span data-ttu-id="22405-158">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="22405-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22405-159">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="22405-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22405-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22405-160">-Confirm</span></span>
<span data-ttu-id="22405-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22405-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22405-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22405-162">-WhatIf</span></span>
<span data-ttu-id="22405-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22405-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22405-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22405-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22405-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22405-165">CommonParameters</span></span>
<span data-ttu-id="22405-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22405-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22405-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22405-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22405-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22405-168">INPUTS</span></span>

### <span data-ttu-id="22405-169">System. String</span><span class="sxs-lookup"><span data-stu-id="22405-169">System.String</span></span>

### <span data-ttu-id="22405-170">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22405-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="22405-171">Microsoft. Azure. Management. keyvault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="22405-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="22405-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22405-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22405-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22405-173">OUTPUTS</span></span>

### <span data-ttu-id="22405-174">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="22405-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="22405-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22405-175">NOTES</span></span>

## <span data-ttu-id="22405-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22405-176">RELATED LINKS</span></span>

[<span data-ttu-id="22405-177">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22405-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="22405-178">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22405-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
