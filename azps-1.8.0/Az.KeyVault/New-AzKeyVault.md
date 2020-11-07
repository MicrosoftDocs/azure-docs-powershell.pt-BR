---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770646"
---
# <span data-ttu-id="2e88e-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2e88e-101">New-AzKeyVault</span></span>

## <span data-ttu-id="2e88e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e88e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e88e-103">Cria um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-103">Creates a key vault.</span></span>

## <span data-ttu-id="2e88e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e88e-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e88e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e88e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e88e-106">O cmdlet **New-AzKeyVault** cria um cofre de chaves no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2e88e-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="2e88e-107">Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="2e88e-108">Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="2e88e-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="2e88e-109">Para obter mais informações, consulte Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="2e88e-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="2e88e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e88e-110">EXAMPLES</span></span>

### <span data-ttu-id="2e88e-111">Exemplo 1: criar um cofre de chaves padrão</span><span class="sxs-lookup"><span data-stu-id="2e88e-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="2e88e-112">Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2e88e-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="2e88e-113">O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14.</span><span class="sxs-lookup"><span data-stu-id="2e88e-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="2e88e-114">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="2e88e-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="2e88e-115">Exemplo 2: criar um cofre de chave Premium</span><span class="sxs-lookup"><span data-stu-id="2e88e-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="2e88e-116">Esse comando cria um cofre de chaves, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2e88e-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="2e88e-117">No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.</span><span class="sxs-lookup"><span data-stu-id="2e88e-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="2e88e-118">OS</span><span class="sxs-lookup"><span data-stu-id="2e88e-118">PARAMETERS</span></span>

### <span data-ttu-id="2e88e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e88e-119">-DefaultProfile</span></span>
<span data-ttu-id="2e88e-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2e88e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e88e-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2e88e-121">-EnabledForDeployment</span></span>
<span data-ttu-id="2e88e-122">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e88e-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="2e88e-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2e88e-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2e88e-124">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="2e88e-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2e88e-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2e88e-126">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="2e88e-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="2e88e-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="2e88e-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="2e88e-128">Se especificado, a proteção contra exclusão imediata estará habilitada para este cofre; requer a exclusão reversível para ser habilitada também.</span><span class="sxs-lookup"><span data-stu-id="2e88e-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="2e88e-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="2e88e-129">-EnableSoftDelete</span></span>
<span data-ttu-id="2e88e-130">Especifica que a funcionalidade de exclusão suave está habilitada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="2e88e-131">Quando a exclusão suave está habilitada, por um período de cortesia, você pode recuperar esse cofre de chaves e seu conteúdo após a exclusão.</span><span class="sxs-lookup"><span data-stu-id="2e88e-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="2e88e-132">Para obter mais informações sobre essa funcionalidade, consulte [visão geral do Azure Key Vault Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="2e88e-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="2e88e-133">Para obter instruções de como fazer, consulte [como usar o virtual Vault Soft-Delete com o PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="2e88e-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="2e88e-134">-Local</span><span class="sxs-lookup"><span data-stu-id="2e88e-134">-Location</span></span>
<span data-ttu-id="2e88e-135">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="2e88e-136">Use o comando [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="2e88e-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="2e88e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e88e-137">-Name</span></span>
<span data-ttu-id="2e88e-138">Especifica o nome do cofre de chaves a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2e88e-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="2e88e-139">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="2e88e-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="2e88e-140">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="2e88e-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="2e88e-141">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2e88e-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="2e88e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e88e-142">-ResourceGroupName</span></span>
<span data-ttu-id="2e88e-143">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="2e88e-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e88e-144">-Sku</span></span>
<span data-ttu-id="2e88e-145">Especifica a SKU da instância do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2e88e-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="2e88e-146">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="2e88e-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="2e88e-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="2e88e-147">-Tag</span></span>
<span data-ttu-id="2e88e-148">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2e88e-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2e88e-149">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2e88e-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2e88e-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e88e-150">-Confirm</span></span>
<span data-ttu-id="2e88e-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e88e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e88e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e88e-152">-WhatIf</span></span>
<span data-ttu-id="2e88e-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e88e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e88e-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e88e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e88e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e88e-155">CommonParameters</span></span>
<span data-ttu-id="2e88e-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e88e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e88e-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e88e-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e88e-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e88e-158">INPUTS</span></span>

### <span data-ttu-id="2e88e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2e88e-159">System.String</span></span>

### <span data-ttu-id="2e88e-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e88e-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e88e-161">Microsoft. Azure. Management. keyvault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="2e88e-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="2e88e-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e88e-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e88e-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e88e-163">OUTPUTS</span></span>

### <span data-ttu-id="2e88e-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2e88e-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2e88e-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e88e-165">NOTES</span></span>

## <span data-ttu-id="2e88e-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e88e-166">RELATED LINKS</span></span>

[<span data-ttu-id="2e88e-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2e88e-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="2e88e-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2e88e-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
