---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 41fcea2b0afc7c18da2f3e4e71764bff1ab2920c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776666"
---
# <span data-ttu-id="73f7b-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="73f7b-101">New-AzKeyVault</span></span>

## <span data-ttu-id="73f7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="73f7b-103">Cria um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-103">Creates a key vault.</span></span>

## <span data-ttu-id="73f7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73f7b-104">SYNTAX</span></span>

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73f7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="73f7b-106">O cmdlet **New-AzKeyVault** cria um cofre de chaves no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="73f7b-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="73f7b-107">Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="73f7b-108">Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="73f7b-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="73f7b-109">Para obter mais informações, consulte Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="73f7b-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="73f7b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73f7b-110">EXAMPLES</span></span>

### <span data-ttu-id="73f7b-111">Exemplo 1: criar um cofre de chaves padrão</span><span class="sxs-lookup"><span data-stu-id="73f7b-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="73f7b-112">Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="73f7b-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="73f7b-113">O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14.</span><span class="sxs-lookup"><span data-stu-id="73f7b-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="73f7b-114">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="73f7b-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="73f7b-115">Exemplo 2: criar um cofre de chave Premium</span><span class="sxs-lookup"><span data-stu-id="73f7b-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="73f7b-116">Esse comando cria um cofre de chaves, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="73f7b-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="73f7b-117">No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.</span><span class="sxs-lookup"><span data-stu-id="73f7b-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="73f7b-118">OS</span><span class="sxs-lookup"><span data-stu-id="73f7b-118">PARAMETERS</span></span>

### <span data-ttu-id="73f7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f7b-119">-DefaultProfile</span></span>
<span data-ttu-id="73f7b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="73f7b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="73f7b-121">-EnabledForDeployment</span></span>
<span data-ttu-id="73f7b-122">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73f7b-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="73f7b-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="73f7b-124">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="73f7b-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="73f7b-126">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="73f7b-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="73f7b-127">-EnableSoftDelete</span></span>
<span data-ttu-id="73f7b-128">Especifica que a funcionalidade de exclusão suave está habilitada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="73f7b-129">Quando a exclusão suave está habilitada, por um período de cortesia, você pode recuperar esse cofre de chaves e seu conteúdo após a exclusão.</span><span class="sxs-lookup"><span data-stu-id="73f7b-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="73f7b-130">Para obter mais informações sobre essa funcionalidade, consulte [visão geral do Azure Key Vault Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="73f7b-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="73f7b-131">Para obter instruções de como fazer, consulte [como usar o virtual Vault Soft-Delete com o PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="73f7b-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-132">-Local</span><span class="sxs-lookup"><span data-stu-id="73f7b-132">-Location</span></span>
<span data-ttu-id="73f7b-133">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="73f7b-134">Use o comando [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="73f7b-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f7b-135">-ResourceGroupName</span></span>
<span data-ttu-id="73f7b-136">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-136">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="73f7b-137">-Sku</span></span>
<span data-ttu-id="73f7b-138">Especifica a SKU da instância do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="73f7b-138">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="73f7b-139">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="73f7b-139">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="73f7b-140">-Tag</span></span>
<span data-ttu-id="73f7b-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="73f7b-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="73f7b-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73f7b-142">For example:</span></span>

<span data-ttu-id="73f7b-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="73f7b-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="73f7b-144">-VaultName</span></span>
<span data-ttu-id="73f7b-145">Especifica o nome do cofre de chaves a ser criado.</span><span class="sxs-lookup"><span data-stu-id="73f7b-145">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="73f7b-146">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="73f7b-146">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="73f7b-147">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="73f7b-147">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="73f7b-148">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="73f7b-148">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73f7b-149">-Confirm</span></span>
<span data-ttu-id="73f7b-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73f7b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f7b-151">-WhatIf</span></span>
<span data-ttu-id="73f7b-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73f7b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f7b-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73f7b-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f7b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f7b-154">CommonParameters</span></span>
<span data-ttu-id="73f7b-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f7b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f7b-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f7b-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f7b-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73f7b-157">INPUTS</span></span>

### <span data-ttu-id="73f7b-158">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73f7b-158">None</span></span>
<span data-ttu-id="73f7b-159">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="73f7b-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73f7b-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73f7b-160">OUTPUTS</span></span>

### <span data-ttu-id="73f7b-161">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="73f7b-161">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="73f7b-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73f7b-162">NOTES</span></span>

## <span data-ttu-id="73f7b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73f7b-163">RELATED LINKS</span></span>

[<span data-ttu-id="73f7b-164">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="73f7b-164">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="73f7b-165">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="73f7b-165">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
