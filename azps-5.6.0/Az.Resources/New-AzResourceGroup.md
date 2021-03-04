---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892728"
---
# <span data-ttu-id="9f572-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f572-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="9f572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f572-102">SYNOPSIS</span></span>
<span data-ttu-id="9f572-103">Cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f572-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="9f572-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f572-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f572-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f572-105">DESCRIPTION</span></span>
<span data-ttu-id="9f572-106">O cmdlet **New-AzResourceGroup** cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f572-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="9f572-107">Você pode criar um grupo de recursos usando apenas um nome e local e, em seguida, usar o cmdlet New-AzResource para criar recursos para adicionar ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="9f572-108">Para adicionar uma implantação a um grupo de recursos existente, use New-AzResourceGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f572-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="9f572-109">Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="9f572-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="9f572-110">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site.</span><span class="sxs-lookup"><span data-stu-id="9f572-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="9f572-111">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="9f572-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="9f572-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f572-112">EXAMPLES</span></span>

### <span data-ttu-id="9f572-113">Exemplo 1: Criar um grupo de recursos vazio</span><span class="sxs-lookup"><span data-stu-id="9f572-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="9f572-114">Este comando cria um grupo de recursos que não tem recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="9f572-115">Você pode usar os cmdlets **New-AzResource** ou **New-AzResourceGroupDeployment** para adicionar recursos e implantações a esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="9f572-116">Exemplo 2: Criar um grupo de recursos vazio usando parâmetros posicionais</span><span class="sxs-lookup"><span data-stu-id="9f572-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="9f572-117">Este comando cria um grupo de recursos que não tem recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="9f572-118">Exemplo 3: Criar um grupo de recursos com marcas</span><span class="sxs-lookup"><span data-stu-id="9f572-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="9f572-119">Este comando cria um grupo de recursos vazio.</span><span class="sxs-lookup"><span data-stu-id="9f572-119">This command creates an empty resource group.</span></span> <span data-ttu-id="9f572-120">Este comando é o mesmo que o comando no Exemplo 1, exceto que ele atribui marcas ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="9f572-121">A primeira marca, chamada Empty, pode ser usada para identificar grupos de recursos que não têm recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="9f572-122">A segunda marca se chama Departamento e tem um valor de Marketing.</span><span class="sxs-lookup"><span data-stu-id="9f572-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="9f572-123">Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.</span><span class="sxs-lookup"><span data-stu-id="9f572-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="9f572-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f572-124">PARAMETERS</span></span>

### <span data-ttu-id="9f572-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9f572-125">-ApiVersion</span></span>
<span data-ttu-id="9f572-126">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9f572-127">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="9f572-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9f572-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f572-128">-DefaultProfile</span></span>
<span data-ttu-id="9f572-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f572-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f572-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9f572-130">-Force</span></span>
<span data-ttu-id="9f572-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9f572-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f572-132">-Location</span><span class="sxs-lookup"><span data-stu-id="9f572-132">-Location</span></span>
<span data-ttu-id="9f572-133">Especifica o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="9f572-134">Especifique um local do data center do Azure, como o Oeste dos EUA ou o Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="9f572-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="9f572-135">Você pode colocar um grupo de recursos em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="9f572-135">You can place a resource group in any location.</span></span> <span data-ttu-id="9f572-136">O grupo de recursos não precisa estar no mesmo local que sua assinatura do Azure ou no mesmo local que seus recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="9f572-137">Para determinar qual local dá suporte a cada tipo de recurso, use o cmdlet Get-AzResourceProvider com o *parâmetro ProviderNamespace.*</span><span class="sxs-lookup"><span data-stu-id="9f572-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="9f572-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9f572-138">-Name</span></span>
<span data-ttu-id="9f572-139">Especifica um nome para o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="9f572-140">O nome do recurso deve ser exclusivo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f572-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="9f572-141">Se um grupo de recursos que já tiver esse nome existir, o comando solicitará a confirmação antes de substituir o grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="9f572-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f572-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f572-142">-Pre</span></span>
<span data-ttu-id="9f572-143">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9f572-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9f572-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f572-144">-Tag</span></span>
<span data-ttu-id="9f572-145">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9f572-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9f572-146">Por exemplo: @{key0="value0";key1=$null;key2="value2"} Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="9f572-147">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro *Tag* de Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor.</span><span class="sxs-lookup"><span data-stu-id="9f572-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="9f572-148">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custos, ou para acompanhar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="9f572-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="9f572-149">Para obter suas marcas predefinidas, use o cmdlet Get-AzTag de usuário.</span><span class="sxs-lookup"><span data-stu-id="9f572-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="9f572-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f572-150">-Confirm</span></span>
<span data-ttu-id="9f572-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f572-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f572-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f572-152">-WhatIf</span></span>
<span data-ttu-id="9f572-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f572-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f572-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f572-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f572-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f572-155">CommonParameters</span></span>
<span data-ttu-id="9f572-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f572-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f572-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f572-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f572-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f572-158">INPUTS</span></span>

### <span data-ttu-id="9f572-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9f572-159">System.String</span></span>

### <span data-ttu-id="9f572-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9f572-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9f572-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f572-161">OUTPUTS</span></span>

### <span data-ttu-id="9f572-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f572-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="9f572-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f572-163">NOTES</span></span>

## <span data-ttu-id="9f572-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f572-164">RELATED LINKS</span></span>

[<span data-ttu-id="9f572-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9f572-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="9f572-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f572-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="9f572-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="9f572-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="9f572-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f572-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="9f572-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f572-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="9f572-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f572-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
