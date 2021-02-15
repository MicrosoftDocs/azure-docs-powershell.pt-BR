---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112627"
---
# <span data-ttu-id="69088-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69088-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="69088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69088-102">SYNOPSIS</span></span>
<span data-ttu-id="69088-103">Modifica um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-103">Modifies a resource group.</span></span>

## <span data-ttu-id="69088-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69088-104">SYNTAX</span></span>

### <span data-ttu-id="69088-105">SetByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="69088-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69088-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="69088-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69088-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="69088-107">DESCRIPTION</span></span>
<span data-ttu-id="69088-108">O **cmdlet Set-AzResourceGroup** modifica as propriedades de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="69088-109">Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="69088-110">*Especifique o parâmetro* Nome para identificar o grupo de recursos e o parâmetro *Marca* para modificar as marcas.</span><span class="sxs-lookup"><span data-stu-id="69088-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="69088-111">Você não pode usar esse cmdlet para alterar o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="69088-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69088-112">EXAMPLES</span></span>

### <span data-ttu-id="69088-113">Exemplo 1: Aplicar uma marca a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69088-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="69088-114">Esse comando aplica uma marca Departamento com um valor de IT a um grupo de recursos que não tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="69088-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="69088-115">Exemplo 2: Adicionar marcas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69088-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="69088-116">Este exemplo adiciona uma marca status com um valor de Aprovado e uma marca FY2016 a um grupo de recursos que tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="69088-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="69088-117">Como as marcas especificadas substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou perdê-las.</span><span class="sxs-lookup"><span data-stu-id="69088-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="69088-118">O primeiro comando obtém o grupo de recursos ContosoRG e usa o método de ponto para obter o valor de sua propriedade Marcas.</span><span class="sxs-lookup"><span data-stu-id="69088-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="69088-119">O comando armazena as marcas na variável $Tags dados.</span><span class="sxs-lookup"><span data-stu-id="69088-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="69088-120">O segundo comando obtém as marcas na variável $Tags dados.</span><span class="sxs-lookup"><span data-stu-id="69088-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="69088-121">O terceiro comando usa o operador de atribuição += para adicionar as marcas Status e FY2016 à matriz de marcas na variável $Tags dados.</span><span class="sxs-lookup"><span data-stu-id="69088-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="69088-122">O quarto comando usa *o* parâmetro Tag do **Set-AzResourceGroup** para aplicar as marcas na variável $Tags ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="69088-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="69088-123">O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="69088-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="69088-124">A saída mostra que o grupo de recursos tem a marca Departamento e as duas novas marcas, Status e FY2015.</span><span class="sxs-lookup"><span data-stu-id="69088-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="69088-125">Exemplo 3: Excluir todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69088-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="69088-126">Esse comando especifica o parâmetro *Marca* com um valor de tabela hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="69088-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="69088-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69088-127">PARAMETERS</span></span>

### <span data-ttu-id="69088-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="69088-128">-ApiVersion</span></span>
<span data-ttu-id="69088-129">Especifica a versão da API com suporte do Provedor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="69088-130">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="69088-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="69088-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69088-131">-DefaultProfile</span></span>
<span data-ttu-id="69088-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="69088-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69088-133">-ID</span><span class="sxs-lookup"><span data-stu-id="69088-133">-Id</span></span>
<span data-ttu-id="69088-134">Especifica a ID do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="69088-134">Specifies the ID of the resource group to modify.</span></span>

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

### <span data-ttu-id="69088-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="69088-135">-Name</span></span>
<span data-ttu-id="69088-136">Especifica o nome do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="69088-136">Specifies the name of the resource group to modify.</span></span>

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

### <span data-ttu-id="69088-137">-Pré-</span><span class="sxs-lookup"><span data-stu-id="69088-137">-Pre</span></span>
<span data-ttu-id="69088-138">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="69088-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="69088-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="69088-139">-Tag</span></span>
<span data-ttu-id="69088-140">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="69088-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="69088-141">Por exemplo: @{key0="value0";key1=$null;key2="value2"} Uma marca é um par nome-valor que você pode criar e aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="69088-142">Depois de atribuir marcas a recursos e  grupos, você pode usar o parâmetro Tag do Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome de marca e valor.</span><span class="sxs-lookup"><span data-stu-id="69088-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="69088-143">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para acompanhar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="69088-144">Para adicionar ou alterar uma marca, você deve substituir o conjunto de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69088-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="69088-145">Para excluir uma marca, insira uma tabela hash com todas as marcas aplicadas no momento ao grupo de recursos, do **Get-AzResourceGroup,** exceto a marca que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="69088-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="69088-146">Para excluir todas as marcas de um grupo de recursos, especifique uma tabela hash vazia: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="69088-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="69088-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69088-147">CommonParameters</span></span>
<span data-ttu-id="69088-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69088-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69088-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69088-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69088-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="69088-150">INPUTS</span></span>

### <span data-ttu-id="69088-151">System.String</span><span class="sxs-lookup"><span data-stu-id="69088-151">System.String</span></span>

### <span data-ttu-id="69088-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="69088-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69088-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="69088-153">OUTPUTS</span></span>

### <span data-ttu-id="69088-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69088-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="69088-155">Notas</span><span class="sxs-lookup"><span data-stu-id="69088-155">NOTES</span></span>

## <span data-ttu-id="69088-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69088-156">RELATED LINKS</span></span>

[<span data-ttu-id="69088-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="69088-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="69088-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69088-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="69088-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69088-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="69088-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69088-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
