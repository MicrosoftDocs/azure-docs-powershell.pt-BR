---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: ad129cfb28aed7670a78550df70d0af410d5dfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429523"
---
# <span data-ttu-id="b88a9-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b88a9-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="b88a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b88a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b88a9-103">Cria um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b88a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b88a9-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b88a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b88a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b88a9-106">O cmdlet **New-AzureRmKeyVault** cria um cofre de chaves no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b88a9-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="b88a9-107">Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="b88a9-108">Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="b88a9-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="b88a9-109">Para obter mais informações, consulte Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="b88a9-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="b88a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b88a9-110">EXAMPLES</span></span>

### <span data-ttu-id="b88a9-111">Exemplo 1: criar um cofre de chaves padrão</span><span class="sxs-lookup"><span data-stu-id="b88a9-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

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

<span data-ttu-id="b88a9-112">Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b88a9-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="b88a9-113">O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14.</span><span class="sxs-lookup"><span data-stu-id="b88a9-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="b88a9-114">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="b88a9-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="b88a9-115">Exemplo 2: criar um cofre de chave Premium</span><span class="sxs-lookup"><span data-stu-id="b88a9-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

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

<span data-ttu-id="b88a9-116">Esse comando cria um cofre de chaves, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="b88a9-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="b88a9-117">No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.</span><span class="sxs-lookup"><span data-stu-id="b88a9-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="b88a9-118">OS</span><span class="sxs-lookup"><span data-stu-id="b88a9-118">PARAMETERS</span></span>

### <span data-ttu-id="b88a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88a9-119">-DefaultProfile</span></span>
<span data-ttu-id="b88a9-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b88a9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88a9-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="b88a9-121">-EnabledForDeployment</span></span>
<span data-ttu-id="b88a9-122">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b88a9-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="b88a9-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b88a9-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="b88a9-124">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="b88a9-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="b88a9-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="b88a9-126">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="b88a9-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="b88a9-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="b88a9-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="b88a9-128">Se especificado, a proteção contra exclusão imediata estará habilitada para este cofre; requer a exclusão reversível para ser habilitada também.</span><span class="sxs-lookup"><span data-stu-id="b88a9-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="b88a9-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="b88a9-129">-EnableSoftDelete</span></span>
<span data-ttu-id="b88a9-130">Especifica que a funcionalidade de exclusão suave está habilitada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="b88a9-131">Quando a exclusão suave está habilitada, por um período de cortesia, você pode recuperar esse cofre de chaves e seu conteúdo após a exclusão.</span><span class="sxs-lookup"><span data-stu-id="b88a9-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="b88a9-132">Para obter mais informações sobre essa funcionalidade, consulte [visão geral do Azure Key Vault Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="b88a9-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="b88a9-133">Para obter instruções de como fazer, consulte [como usar o virtual Vault Soft-Delete com o PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="b88a9-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="b88a9-134">-Local</span><span class="sxs-lookup"><span data-stu-id="b88a9-134">-Location</span></span>
<span data-ttu-id="b88a9-135">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="b88a9-136">Use o comando [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="b88a9-136">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

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

### <span data-ttu-id="b88a9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="b88a9-137">-Name</span></span>
<span data-ttu-id="b88a9-138">Especifica o nome do cofre de chaves a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b88a9-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="b88a9-139">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="b88a9-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="b88a9-140">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="b88a9-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="b88a9-141">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b88a9-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="b88a9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88a9-142">-ResourceGroupName</span></span>
<span data-ttu-id="b88a9-143">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="b88a9-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="b88a9-144">-Sku</span></span>
<span data-ttu-id="b88a9-145">Especifica a SKU da instância do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b88a9-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="b88a9-146">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="b88a9-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="b88a9-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="b88a9-147">-Tag</span></span>
<span data-ttu-id="b88a9-148">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b88a9-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b88a9-149">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b88a9-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b88a9-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b88a9-150">-Confirm</span></span>
<span data-ttu-id="b88a9-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b88a9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b88a9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b88a9-152">-WhatIf</span></span>
<span data-ttu-id="b88a9-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b88a9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b88a9-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b88a9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b88a9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88a9-155">CommonParameters</span></span>
<span data-ttu-id="b88a9-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88a9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88a9-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b88a9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88a9-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b88a9-158">INPUTS</span></span>

### <span data-ttu-id="b88a9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="b88a9-159">System.String</span></span>

### <span data-ttu-id="b88a9-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b88a9-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b88a9-161">Microsoft. Azure. Management. keyvault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="b88a9-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="b88a9-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b88a9-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b88a9-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b88a9-163">OUTPUTS</span></span>

### <span data-ttu-id="b88a9-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b88a9-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="b88a9-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b88a9-165">NOTES</span></span>

## <span data-ttu-id="b88a9-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b88a9-166">RELATED LINKS</span></span>

[<span data-ttu-id="b88a9-167">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b88a9-167">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="b88a9-168">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b88a9-168">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)