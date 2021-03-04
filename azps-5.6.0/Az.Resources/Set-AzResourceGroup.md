---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891092"
---
# <span data-ttu-id="71793-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71793-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="71793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71793-102">SYNOPSIS</span></span>
<span data-ttu-id="71793-103">Modifica um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-103">Modifies a resource group.</span></span>

## <span data-ttu-id="71793-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71793-104">SYNTAX</span></span>

### <span data-ttu-id="71793-105">SetByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71793-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71793-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="71793-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71793-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71793-107">DESCRIPTION</span></span>
<span data-ttu-id="71793-108">O cmdlet **Set-AzResourceGroup** modifica as propriedades de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="71793-109">Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="71793-110">*Especifique o parâmetro Name* para identificar o grupo de recursos e o parâmetro *Tag* para modificar as marcas.</span><span class="sxs-lookup"><span data-stu-id="71793-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="71793-111">Não é possível usar esse cmdlet para alterar o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="71793-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71793-112">EXAMPLES</span></span>

### <span data-ttu-id="71793-113">Exemplo 1: Aplicar uma marca a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71793-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="71793-114">Este comando aplica uma marca Department com um valor de IT a um grupo de recursos que não tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="71793-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="71793-115">Exemplo 2: Adicionar marcas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71793-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="71793-116">Este exemplo adiciona uma marca Status com um valor aprovado e uma marca FY2016 a um grupo de recursos que possui marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="71793-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="71793-117">Como as marcas especificadas substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou você as perderá.</span><span class="sxs-lookup"><span data-stu-id="71793-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="71793-118">O primeiro comando obtém o grupo de recursos ContosoRG e usa o método dot para obter o valor de sua propriedade Tags.</span><span class="sxs-lookup"><span data-stu-id="71793-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="71793-119">O comando armazena as marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="71793-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="71793-120">O segundo comando obtém as marcas na $Tags variável.</span><span class="sxs-lookup"><span data-stu-id="71793-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="71793-121">O terceiro comando usa o operador de atribuição += para adicionar as marcas Status e FY2016 à matriz de marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="71793-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="71793-122">O quarto comando usa o parâmetro *Tag* de **Set-AzResourceGroup** para aplicar as marcas na variável $Tags ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="71793-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="71793-123">O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="71793-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="71793-124">A saída mostra que o grupo de recursos tem a marca Department e as duas novas marcas, Status e FY2015.</span><span class="sxs-lookup"><span data-stu-id="71793-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="71793-125">Exemplo 3: Excluir todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71793-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="71793-126">Este comando especifica o parâmetro *Tag com* um valor de tabela de hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="71793-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="71793-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71793-127">PARAMETERS</span></span>

### <span data-ttu-id="71793-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71793-128">-ApiVersion</span></span>
<span data-ttu-id="71793-129">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="71793-130">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="71793-130">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71793-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71793-131">-DefaultProfile</span></span>
<span data-ttu-id="71793-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="71793-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71793-133">-Id</span><span class="sxs-lookup"><span data-stu-id="71793-133">-Id</span></span>
<span data-ttu-id="71793-134">Especifica a ID do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="71793-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71793-135">-Name</span><span class="sxs-lookup"><span data-stu-id="71793-135">-Name</span></span>
<span data-ttu-id="71793-136">Especifica o nome do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="71793-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71793-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="71793-137">-Pre</span></span>
<span data-ttu-id="71793-138">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="71793-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71793-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="71793-139">-Tag</span></span>
<span data-ttu-id="71793-140">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71793-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="71793-141">Por exemplo: @{key0="value0";key1=$null;key2="value2"} Uma marca é um par de valores de nome que você pode criar e aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="71793-142">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro *Tag* de Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome e valor da marca.</span><span class="sxs-lookup"><span data-stu-id="71793-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="71793-143">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custos, ou para acompanhar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="71793-144">Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71793-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="71793-145">Para excluir uma marca, insira uma tabela de hash com todas as marcas atualmente aplicadas ao grupo de recursos, de **Get-AzResourceGroup**, exceto pela marca que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="71793-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="71793-146">Para excluir todas as marcas de um grupo de recursos, especifique uma tabela de hash vazia: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="71793-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71793-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71793-147">CommonParameters</span></span>
<span data-ttu-id="71793-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71793-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71793-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71793-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71793-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71793-150">INPUTS</span></span>

### <span data-ttu-id="71793-151">System.String</span><span class="sxs-lookup"><span data-stu-id="71793-151">System.String</span></span>

### <span data-ttu-id="71793-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="71793-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71793-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71793-153">OUTPUTS</span></span>

### <span data-ttu-id="71793-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71793-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="71793-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="71793-155">NOTES</span></span>

## <span data-ttu-id="71793-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71793-156">RELATED LINKS</span></span>

[<span data-ttu-id="71793-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="71793-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="71793-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71793-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="71793-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71793-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="71793-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71793-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
