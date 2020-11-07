---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776314"
---
# <span data-ttu-id="cf549-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf549-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="cf549-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf549-102">SYNOPSIS</span></span>
<span data-ttu-id="cf549-103">Modifica um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-103">Modifies a resource group.</span></span>

## <span data-ttu-id="cf549-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf549-104">SYNTAX</span></span>

### <span data-ttu-id="cf549-105">SetByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf549-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf549-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cf549-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf549-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf549-107">DESCRIPTION</span></span>
<span data-ttu-id="cf549-108">O cmdlet **set-AzResourceGroup** modifica as propriedades de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="cf549-109">Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="cf549-110">Especifique o parâmetro *Name* para identificar o grupo de recursos e o parâmetro de *marca* para modificar as marcas.</span><span class="sxs-lookup"><span data-stu-id="cf549-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="cf549-111">Você não pode usar esse cmdlet para alterar o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="cf549-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf549-112">EXAMPLES</span></span>

### <span data-ttu-id="cf549-113">Exemplo 1: aplicar uma marca a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf549-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="cf549-114">Esse comando aplica uma marca de departamento com um valor a um grupo de recursos que não tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="cf549-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="cf549-115">Exemplo 2: adicionar marcas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf549-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="cf549-116">Este exemplo adiciona uma marca de status com um valor de approved e uma marca FY2016 a um grupo de recursos que tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="cf549-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="cf549-117">Como as marcas que você especifica substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou perdê-las.</span><span class="sxs-lookup"><span data-stu-id="cf549-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="cf549-118">O primeiro comando obtém o grupo de recursos ContosoRG e usa o método dot para obter o valor de sua propriedade Tags.</span><span class="sxs-lookup"><span data-stu-id="cf549-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="cf549-119">O comando armazena as marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="cf549-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="cf549-120">O segundo comando obtém as marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="cf549-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="cf549-121">O terceiro comando usa o operador de atribuição + = para adicionar as marcas status e FY2016 à matriz de marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="cf549-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="cf549-122">O quarto comando usa o parâmetro de *marca* de **set-AzResourceGroup** para aplicar as marcas na variável $Tags para o grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="cf549-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="cf549-123">O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="cf549-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="cf549-124">A saída mostra que o grupo de recursos tem a marca de departamento e as duas novas marcas, status e FY2015.</span><span class="sxs-lookup"><span data-stu-id="cf549-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="cf549-125">Exemplo 3: excluir todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf549-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="cf549-126">Esse comando especifica o parâmetro de *marca* com um valor de tabela de hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="cf549-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="cf549-127">OS</span><span class="sxs-lookup"><span data-stu-id="cf549-127">PARAMETERS</span></span>

### <span data-ttu-id="cf549-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cf549-128">-ApiVersion</span></span>
<span data-ttu-id="cf549-129">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cf549-130">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="cf549-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cf549-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf549-131">-DefaultProfile</span></span>
<span data-ttu-id="cf549-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cf549-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf549-133">-ID</span><span class="sxs-lookup"><span data-stu-id="cf549-133">-Id</span></span>
<span data-ttu-id="cf549-134">Especifica a ID do grupo de recursos a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="cf549-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf549-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf549-135">-Name</span></span>
<span data-ttu-id="cf549-136">Especifica o nome do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="cf549-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf549-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="cf549-137">-Pre</span></span>
<span data-ttu-id="cf549-138">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="cf549-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cf549-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="cf549-139">-Tag</span></span>
<span data-ttu-id="cf549-140">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cf549-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cf549-141">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} uma marca é um par de nome-valor que você pode criar e aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="cf549-142">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome da marca ou valor.</span><span class="sxs-lookup"><span data-stu-id="cf549-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="cf549-143">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="cf549-144">Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf549-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="cf549-145">Para excluir uma marca, insira uma tabela de hash com todas as marcas aplicadas atualmente ao grupo de recursos, do **Get-AzResourceGroup** , exceto para a marca que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="cf549-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="cf549-146">Para excluir todas as marcas de um grupo de recursos, especifique uma tabela de hash vazia: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="cf549-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="cf549-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf549-147">CommonParameters</span></span>
<span data-ttu-id="cf549-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf549-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf549-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf549-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf549-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf549-150">INPUTS</span></span>

### <span data-ttu-id="cf549-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cf549-151">None</span></span>

## <span data-ttu-id="cf549-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf549-152">OUTPUTS</span></span>

### <span data-ttu-id="cf549-153">Microsoft. Azure. Commands. Resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf549-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="cf549-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf549-154">NOTES</span></span>

## <span data-ttu-id="cf549-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf549-155">RELATED LINKS</span></span>

[<span data-ttu-id="cf549-156">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cf549-156">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="cf549-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf549-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="cf549-158">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf549-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="cf549-159">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf549-159">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)