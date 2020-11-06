---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610175"
---
# <span data-ttu-id="40e82-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40e82-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="40e82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40e82-102">SYNOPSIS</span></span>
<span data-ttu-id="40e82-103">Modifica um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40e82-104">SYNTAX</span></span>

### <span data-ttu-id="40e82-105">Lista o grupo de recursos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="40e82-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="40e82-106">Assume</span><span class="sxs-lookup"><span data-stu-id="40e82-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e82-107">Lista o grupo de recursos com base na ID.</span><span class="sxs-lookup"><span data-stu-id="40e82-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e82-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40e82-108">DESCRIPTION</span></span>
<span data-ttu-id="40e82-109">O cmdlet **set-AzureRmResourceGroup** modifica as propriedades de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="40e82-110">Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="40e82-111">Especifique o parâmetro *Name* para identificar o grupo de recursos e o parâmetro de *marca* para modificar as marcas.</span><span class="sxs-lookup"><span data-stu-id="40e82-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="40e82-112">Você não pode usar esse cmdlet para alterar o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="40e82-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40e82-113">EXAMPLES</span></span>

### <span data-ttu-id="40e82-114">Exemplo 1: aplicar uma marca a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="40e82-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="40e82-115">Esse comando aplica uma marca de departamento com um valor a um grupo de recursos que não tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="40e82-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="40e82-116">Exemplo 2: adicionar marcas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="40e82-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="40e82-117">Este exemplo adiciona uma marca de status com um valor de approved e uma marca FY2016 a um grupo de recursos que tem marcas existentes.</span><span class="sxs-lookup"><span data-stu-id="40e82-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="40e82-118">Como as marcas que você especifica substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou perdê-las.</span><span class="sxs-lookup"><span data-stu-id="40e82-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="40e82-119">O primeiro comando obtém o grupo de recursos ContosoRG e usa o método dot para obter o valor de sua propriedade Tags.</span><span class="sxs-lookup"><span data-stu-id="40e82-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="40e82-120">O comando armazena as marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="40e82-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="40e82-121">O segundo comando obtém as marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="40e82-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="40e82-122">O terceiro comando usa o operador de atribuição + = para adicionar as marcas status e FY2016 à matriz de marcas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="40e82-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="40e82-123">O quarto comando usa o parâmetro de *marca* de **set-AzureRmResourceGroup** para aplicar as marcas na variável $Tags para o grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="40e82-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="40e82-124">O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="40e82-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="40e82-125">A saída mostra que o grupo de recursos tem a marca de departamento e as duas novas marcas, status e FY2015.</span><span class="sxs-lookup"><span data-stu-id="40e82-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="40e82-126">Exemplo 3: excluir todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="40e82-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="40e82-127">Esse comando especifica o parâmetro de *marca* com um valor de tabela de hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="40e82-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="40e82-128">OS</span><span class="sxs-lookup"><span data-stu-id="40e82-128">PARAMETERS</span></span>

### <span data-ttu-id="40e82-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="40e82-129">-ApiVersion</span></span>
<span data-ttu-id="40e82-130">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="40e82-131">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="40e82-131">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="40e82-132">-ID</span><span class="sxs-lookup"><span data-stu-id="40e82-132">-Id</span></span>
<span data-ttu-id="40e82-133">Especifica a ID do grupo de recursos a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="40e82-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e82-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="40e82-134">-Name</span></span>
<span data-ttu-id="40e82-135">Especifica o nome do grupo de recursos a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="40e82-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e82-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="40e82-136">-Pre</span></span>
<span data-ttu-id="40e82-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="40e82-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="40e82-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="40e82-138">-Tag</span></span>
<span data-ttu-id="40e82-139">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="40e82-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40e82-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="40e82-140">For example:</span></span>

<span data-ttu-id="40e82-141">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="40e82-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="40e82-142">Uma marca é um par de nome-valor que você pode criar e aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="40e82-143">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzureRmResource e Get-AzureRmResourceGroup para pesquisar recursos e grupos por nome ou nome da marca ou valor.</span><span class="sxs-lookup"><span data-stu-id="40e82-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="40e82-144">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="40e82-145">Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e82-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="40e82-146">Para excluir uma marca, insira uma tabela de hash com todas as marcas aplicadas atualmente ao grupo de recursos, do **Get-AzureRmResourceGroup** , exceto para a marca que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="40e82-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="40e82-147">Para excluir todas as marcas de um grupo de recursos, especifique uma tabela de hash vazia: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="40e82-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="40e82-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e82-148">-DefaultProfile</span></span>
<span data-ttu-id="40e82-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40e82-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e82-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e82-150">CommonParameters</span></span>
<span data-ttu-id="40e82-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e82-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e82-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e82-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e82-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40e82-153">INPUTS</span></span>

### <span data-ttu-id="40e82-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40e82-154">None</span></span>

## <span data-ttu-id="40e82-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40e82-155">OUTPUTS</span></span>

### <span data-ttu-id="40e82-156">Microsoft. Azure. Commands. Resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40e82-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="40e82-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40e82-157">NOTES</span></span>

## <span data-ttu-id="40e82-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e82-158">RELATED LINKS</span></span>

[<span data-ttu-id="40e82-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="40e82-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="40e82-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40e82-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="40e82-161">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40e82-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="40e82-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40e82-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
