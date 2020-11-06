---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441043"
---
# <span data-ttu-id="7553c-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="7553c-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="7553c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7553c-102">SYNOPSIS</span></span>
<span data-ttu-id="7553c-103">Cria um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7553c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7553c-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7553c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7553c-105">DESCRIPTION</span></span>
<span data-ttu-id="7553c-106">O cmdlet **New-AzureRmKeyVault** cria um cofre de chaves no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7553c-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="7553c-107">Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="7553c-108">Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="7553c-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="7553c-109">Para obter mais informações, consulte Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="7553c-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="7553c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7553c-110">EXAMPLES</span></span>

### <span data-ttu-id="7553c-111">Exemplo 1: criar um cofre de chaves padrão</span><span class="sxs-lookup"><span data-stu-id="7553c-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="7553c-112">Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="7553c-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="7553c-113">O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14.</span><span class="sxs-lookup"><span data-stu-id="7553c-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="7553c-114">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="7553c-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="7553c-115">Exemplo 2: criar um cofre de chave Premium</span><span class="sxs-lookup"><span data-stu-id="7553c-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="7553c-116">Esse comando cria um cofre de chaves, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7553c-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="7553c-117">No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.</span><span class="sxs-lookup"><span data-stu-id="7553c-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="7553c-118">OS</span><span class="sxs-lookup"><span data-stu-id="7553c-118">PARAMETERS</span></span>

### <span data-ttu-id="7553c-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7553c-119">-EnabledForDeployment</span></span>
<span data-ttu-id="7553c-120">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7553c-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="7553c-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7553c-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7553c-122">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="7553c-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7553c-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7553c-124">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="7553c-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="7553c-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="7553c-125">-EnableSoftDelete</span></span>
<span data-ttu-id="7553c-126">Se especificado, a funcionalidade ' exclusão reversível ' está habilitada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

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

### <span data-ttu-id="7553c-127">-Local</span><span class="sxs-lookup"><span data-stu-id="7553c-127">-Location</span></span>
<span data-ttu-id="7553c-128">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="7553c-129">Use o comando Get-AzureLocation ( https://msdn.microsoft.com/ library/Azure/mt589064. aspx) para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="7553c-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="7553c-130">Para obter mais informações, digite `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="7553c-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7553c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7553c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7553c-132">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="7553c-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="7553c-133">-Sku</span></span>
<span data-ttu-id="7553c-134">Especifica a SKU da instância do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7553c-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="7553c-135">Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="7553c-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="7553c-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="7553c-136">-Tag</span></span>
<span data-ttu-id="7553c-137">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7553c-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7553c-138">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7553c-138">For example:</span></span>

<span data-ttu-id="7553c-139">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7553c-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7553c-140">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="7553c-140">-VaultName</span></span>
<span data-ttu-id="7553c-141">Especifica o nome do cofre de chaves a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7553c-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="7553c-142">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="7553c-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="7553c-143">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="7553c-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="7553c-144">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7553c-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="7553c-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7553c-145">-Confirm</span></span>
<span data-ttu-id="7553c-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7553c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7553c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7553c-147">-WhatIf</span></span>
<span data-ttu-id="7553c-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7553c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7553c-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7553c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7553c-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7553c-150">-DefaultProfile</span></span>
<span data-ttu-id="7553c-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7553c-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7553c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7553c-152">CommonParameters</span></span>
<span data-ttu-id="7553c-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7553c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7553c-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7553c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7553c-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7553c-155">INPUTS</span></span>

## <span data-ttu-id="7553c-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7553c-156">OUTPUTS</span></span>

### <span data-ttu-id="7553c-157">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="7553c-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="7553c-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7553c-158">NOTES</span></span>

## <span data-ttu-id="7553c-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7553c-159">RELATED LINKS</span></span>

[<span data-ttu-id="7553c-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="7553c-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="7553c-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="7553c-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
