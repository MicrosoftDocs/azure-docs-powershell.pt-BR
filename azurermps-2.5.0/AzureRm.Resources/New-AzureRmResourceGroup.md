---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: dd115a7d0445a7b07557b884dd2c7413f5269d00
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786232"
---
# <span data-ttu-id="4d190-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d190-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="4d190-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d190-102">SYNOPSIS</span></span>
<span data-ttu-id="4d190-103">Cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d190-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d190-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d190-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d190-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d190-105">DESCRIPTION</span></span>
<span data-ttu-id="4d190-106">O cmdlet **New-AzureRmResourceGroup** cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d190-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="4d190-107">Você pode criar um grupo de recursos usando apenas um nome e um local e, em seguida, usar o cmdlet New-AzureRmResource para criar recursos a serem adicionados ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="4d190-108">Para adicionar uma implantação a um grupo de recursos existente, use o cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="4d190-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="4d190-109">Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="4d190-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="4d190-110">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site.</span><span class="sxs-lookup"><span data-stu-id="4d190-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="4d190-111">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="4d190-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="4d190-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d190-112">EXAMPLES</span></span>

### <span data-ttu-id="4d190-113">Exemplo 1: criar um grupo de recursos vazio</span><span class="sxs-lookup"><span data-stu-id="4d190-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="4d190-114">Esse comando cria um grupo de recursos sem recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="4d190-115">Você pode usar os cmdlets **New-AzureRmResource** ou **New-AzureRmResourceGroupDeployment** para adicionar recursos e implantações a este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="4d190-116">Exemplo 2: criar um grupo de recursos vazios usando parâmetros de posição</span><span class="sxs-lookup"><span data-stu-id="4d190-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="4d190-117">Esse comando cria um grupo de recursos sem recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="4d190-118">Exemplo 3: criar um grupo de recursos com marcas</span><span class="sxs-lookup"><span data-stu-id="4d190-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="4d190-119">Esse comando cria um grupo de recursos vazios.</span><span class="sxs-lookup"><span data-stu-id="4d190-119">This command creates an empty resource group.</span></span> <span data-ttu-id="4d190-120">Esse comando é o mesmo que o comando no exemplo 1, exceto que ele atribui marcas ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="4d190-121">A primeira marca, denominada Empty, pode ser usada para identificar grupos de recursos que não têm recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="4d190-122">A segunda marca é nomeada departamento e tem um valor de marketing.</span><span class="sxs-lookup"><span data-stu-id="4d190-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="4d190-123">Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.</span><span class="sxs-lookup"><span data-stu-id="4d190-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="4d190-124">OS</span><span class="sxs-lookup"><span data-stu-id="4d190-124">PARAMETERS</span></span>

### <span data-ttu-id="4d190-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d190-125">-ApiVersion</span></span>
<span data-ttu-id="4d190-126">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4d190-127">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="4d190-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4d190-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d190-128">-DefaultProfile</span></span>
<span data-ttu-id="4d190-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4d190-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d190-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4d190-130">-Force</span></span>
<span data-ttu-id="4d190-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d190-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d190-132">-Local</span><span class="sxs-lookup"><span data-stu-id="4d190-132">-Location</span></span>
<span data-ttu-id="4d190-133">Especifica o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="4d190-134">Especifique um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="4d190-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="4d190-135">Você pode colocar um grupo de recursos em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="4d190-135">You can place a resource group in any location.</span></span> <span data-ttu-id="4d190-136">O grupo de recursos não precisa estar no mesmo local de sua assinatura do Azure ou no mesmo local de seus recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="4d190-137">Para determinar qual local oferece suporte a cada tipo de recurso, use o cmdlet Get-AzureRmResourceProvider com o parâmetro *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="4d190-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d190-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d190-138">-Name</span></span>
<span data-ttu-id="4d190-139">Especifica um nome para o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="4d190-140">O nome do recurso deve ser exclusivo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4d190-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="4d190-141">Se um grupo de recursos com esse nome já existir, o comando solicitará confirmação antes de substituir o grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="4d190-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d190-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d190-142">-Pre</span></span>
<span data-ttu-id="4d190-143">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4d190-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4d190-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="4d190-144">-Tag</span></span>
<span data-ttu-id="4d190-145">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4d190-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d190-146">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="4d190-147">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzureRmResource e Get-AzureRmResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor.</span><span class="sxs-lookup"><span data-stu-id="4d190-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="4d190-148">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="4d190-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="4d190-149">Para obter suas marcas predefinidas, use o cmdlet Get-AzureRMTag.</span><span class="sxs-lookup"><span data-stu-id="4d190-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="4d190-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d190-150">-Confirm</span></span>
<span data-ttu-id="4d190-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d190-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d190-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d190-152">-WhatIf</span></span>
<span data-ttu-id="4d190-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d190-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d190-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d190-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d190-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d190-155">CommonParameters</span></span>
<span data-ttu-id="4d190-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d190-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d190-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d190-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d190-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d190-158">INPUTS</span></span>

### <span data-ttu-id="4d190-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4d190-159">None</span></span>

## <span data-ttu-id="4d190-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d190-160">OUTPUTS</span></span>

### <span data-ttu-id="4d190-161">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d190-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="4d190-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d190-162">NOTES</span></span>

## <span data-ttu-id="4d190-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d190-163">RELATED LINKS</span></span>

[<span data-ttu-id="4d190-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4d190-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="4d190-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d190-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="4d190-166">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4d190-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="4d190-167">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d190-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="4d190-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d190-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="4d190-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d190-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
