---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116722"
---
# <span data-ttu-id="2c51a-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2c51a-101">New-AzKeyVault</span></span>

## <span data-ttu-id="2c51a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c51a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c51a-103">Cria um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="2c51a-103">Creates a key vault.</span></span>

## <span data-ttu-id="2c51a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c51a-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c51a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c51a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c51a-106">O **cmdlet New-AzKeyVault** cria um cofre de chave no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2c51a-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="2c51a-107">Este cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2c51a-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="2c51a-108">Observação: se você vir o erro A assinatura não está registrada para usar o **namespace 'Microsoft.KeyVault'** ao tentar criar seu novo cofre de chave, execute **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** e execute novamente o comando **New-AzKeyVault.**</span><span class="sxs-lookup"><span data-stu-id="2c51a-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="2c51a-109">Para obter mais informações, consulte Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="2c51a-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="2c51a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c51a-110">EXAMPLES</span></span>

### <span data-ttu-id="2c51a-111">Exemplo 1: Criar um cofre de chave Padrão</span><span class="sxs-lookup"><span data-stu-id="2c51a-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="2c51a-112">Esse comando cria um cofre de chave chamado Contoso03Vault, na região leste dos EUA do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c51a-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="2c51a-113">O comando adiciona o cofre de chave ao grupo de recursos chamado Grupo14.</span><span class="sxs-lookup"><span data-stu-id="2c51a-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="2c51a-114">Como o comando não especifica um valor para o parâmetro *SKU,* ele cria um cofre de chave Padrão.</span><span class="sxs-lookup"><span data-stu-id="2c51a-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="2c51a-115">Exemplo 2: Criar um cofre de tecla Premium</span><span class="sxs-lookup"><span data-stu-id="2c51a-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="2c51a-116">Esse comando cria um cofre de teclas, assim como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2c51a-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="2c51a-117">No entanto, especifica um valor premium para o parâmetro *SKU* para criar um cofre de tecla Premium.</span><span class="sxs-lookup"><span data-stu-id="2c51a-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="2c51a-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2c51a-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="2c51a-119">Criar um cofre de chave e especificar regras de rede para permitir o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="2c51a-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="2c51a-120">Confira `New-AzKeyVaultNetworkRuleSetObject` mais informações.</span><span class="sxs-lookup"><span data-stu-id="2c51a-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="2c51a-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c51a-121">PARAMETERS</span></span>

### <span data-ttu-id="2c51a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c51a-122">-DefaultProfile</span></span>
<span data-ttu-id="2c51a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2c51a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c51a-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2c51a-124">-EnabledForDeployment</span></span>
<span data-ttu-id="2c51a-125">Permite que o provedor de recursos Microsoft.Compute recupere segredos desse cofre-chave quando esse cofre de chave é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2c51a-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="2c51a-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2c51a-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2c51a-127">Habilita o serviço de criptografia de disco do Azure a obter segredos e desembrulhar chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2c51a-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="2c51a-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2c51a-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2c51a-129">Permite que o Gerenciador de Recursos do Azure receba segredos desse cofre de chave quando esse cofre de chave for referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="2c51a-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="2c51a-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="2c51a-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="2c51a-131">Se especificado, a proteção contra exclusão imediata está habilitada para este cofre; requer que a exclusão suave também seja habilitada.</span><span class="sxs-lookup"><span data-stu-id="2c51a-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="2c51a-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="2c51a-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="2c51a-133">Se especificado, permite autorizar ações de dados por RBAC (Controle de Acesso Baseado em Função) e, em seguida, as políticas de acesso especificadas nas propriedades do cofre serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="2c51a-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="2c51a-134">Observe que as ações de gerenciamento são sempre autorizadas com RBAC.</span><span class="sxs-lookup"><span data-stu-id="2c51a-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="2c51a-135">-Local</span><span class="sxs-lookup"><span data-stu-id="2c51a-135">-Location</span></span>
<span data-ttu-id="2c51a-136">Especifica a região do Azure na qual criar o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="2c51a-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="2c51a-137">Use o comando [Get-AzLocation para](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) ver suas escolhas.</span><span class="sxs-lookup"><span data-stu-id="2c51a-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="2c51a-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c51a-138">-Name</span></span>
<span data-ttu-id="2c51a-139">Especifica um nome do cofre de chave a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2c51a-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="2c51a-140">O nome pode ser qualquer combinação de letras, dígitos ou hífens.</span><span class="sxs-lookup"><span data-stu-id="2c51a-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="2c51a-141">O nome deve começar e terminar com uma letra ou dígito.</span><span class="sxs-lookup"><span data-stu-id="2c51a-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="2c51a-142">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2c51a-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="2c51a-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c51a-143">-NetworkRuleSet</span></span>
<span data-ttu-id="2c51a-144">Especifica o conjunto de regras de rede do cofre.</span><span class="sxs-lookup"><span data-stu-id="2c51a-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="2c51a-145">Ele rege a acessibilidade do cofre de chave de locais de rede específicos.</span><span class="sxs-lookup"><span data-stu-id="2c51a-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="2c51a-146">Criado por `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="2c51a-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="2c51a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c51a-147">-ResourceGroupName</span></span>
<span data-ttu-id="2c51a-148">Especifica o nome de um grupo de recursos existente no qual se cria o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="2c51a-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="2c51a-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="2c51a-149">-Sku</span></span>
<span data-ttu-id="2c51a-150">Especifica a SKU da instância do cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="2c51a-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="2c51a-151">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de Preços do Cofre de Chave do Azure ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="2c51a-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c51a-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2c51a-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="2c51a-153">Especifica por quanto tempo os recursos excluídos são retidos e por quanto tempo um cofre ou objeto no estado excluído pode ser limpo.</span><span class="sxs-lookup"><span data-stu-id="2c51a-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="2c51a-154">O padrão é de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="2c51a-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="2c51a-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c51a-155">-Tag</span></span>
<span data-ttu-id="2c51a-156">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2c51a-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c51a-157">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2c51a-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2c51a-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c51a-158">-Confirm</span></span>
<span data-ttu-id="2c51a-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c51a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c51a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c51a-160">-WhatIf</span></span>
<span data-ttu-id="2c51a-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c51a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c51a-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c51a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c51a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c51a-163">CommonParameters</span></span>
<span data-ttu-id="2c51a-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c51a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c51a-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c51a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c51a-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c51a-166">INPUTS</span></span>

### <span data-ttu-id="2c51a-167">System.String</span><span class="sxs-lookup"><span data-stu-id="2c51a-167">System.String</span></span>

### <span data-ttu-id="2c51a-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2c51a-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2c51a-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="2c51a-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="2c51a-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2c51a-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2c51a-171">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c51a-171">OUTPUTS</span></span>

### <span data-ttu-id="2c51a-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2c51a-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2c51a-173">Notas</span><span class="sxs-lookup"><span data-stu-id="2c51a-173">NOTES</span></span>

## <span data-ttu-id="2c51a-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c51a-174">RELATED LINKS</span></span>

[<span data-ttu-id="2c51a-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2c51a-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="2c51a-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2c51a-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
