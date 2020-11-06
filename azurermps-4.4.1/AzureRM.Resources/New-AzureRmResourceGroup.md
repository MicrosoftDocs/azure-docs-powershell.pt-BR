---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430666"
---
# <span data-ttu-id="d40d6-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d40d6-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="d40d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d40d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d40d6-103">Cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d40d6-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d40d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d40d6-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d40d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d40d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d40d6-106">O cmdlet **New-AzureRmResourceGroup** cria um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d40d6-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="d40d6-107">Você pode criar um grupo de recursos usando apenas um nome e um local e, em seguida, usar o cmdlet New-AzureRmResource para criar recursos a serem adicionados ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="d40d6-108">Para adicionar uma implantação a um grupo de recursos existente, use o cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d40d6-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="d40d6-109">Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="d40d6-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="d40d6-110">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site.</span><span class="sxs-lookup"><span data-stu-id="d40d6-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="d40d6-111">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="d40d6-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="d40d6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d40d6-112">EXAMPLES</span></span>

### <span data-ttu-id="d40d6-113">Exemplo 1: criar um grupo de recursos vazio</span><span class="sxs-lookup"><span data-stu-id="d40d6-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="d40d6-114">Esse comando cria um grupo de recursos sem recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="d40d6-115">Você pode usar os cmdlets **New-AzureRmResource** ou **New-AzureRmResourceGroupDeployment** para adicionar recursos e implantações a este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="d40d6-116">Exemplo 2: criar um grupo de recursos com marcas</span><span class="sxs-lookup"><span data-stu-id="d40d6-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="d40d6-117">Esse comando cria um grupo de recursos vazios.</span><span class="sxs-lookup"><span data-stu-id="d40d6-117">This command creates an empty resource group.</span></span> <span data-ttu-id="d40d6-118">Esse comando é o mesmo que o comando no exemplo 1, exceto que ele atribui marcas ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="d40d6-119">A primeira marca, denominada Empty, pode ser usada para identificar grupos de recursos que não têm recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="d40d6-120">A segunda marca é nomeada departamento e tem um valor de marketing.</span><span class="sxs-lookup"><span data-stu-id="d40d6-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="d40d6-121">Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.</span><span class="sxs-lookup"><span data-stu-id="d40d6-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="d40d6-122">OS</span><span class="sxs-lookup"><span data-stu-id="d40d6-122">PARAMETERS</span></span>

### <span data-ttu-id="d40d6-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d40d6-123">-ApiVersion</span></span>
<span data-ttu-id="d40d6-124">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d40d6-125">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="d40d6-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d40d6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d40d6-126">-Force</span></span>
<span data-ttu-id="d40d6-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d40d6-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d40d6-128">-Local</span><span class="sxs-lookup"><span data-stu-id="d40d6-128">-Location</span></span>
<span data-ttu-id="d40d6-129">Especifica o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="d40d6-130">Especifique um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="d40d6-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="d40d6-131">Você pode colocar um grupo de recursos em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="d40d6-131">You can place a resource group in any location.</span></span> <span data-ttu-id="d40d6-132">O grupo de recursos não precisa estar no mesmo local de sua assinatura do Azure ou no mesmo local de seus recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="d40d6-133">Para determinar qual local oferece suporte a cada tipo de recurso, use o cmdlet Get-AzureRmResourceProvider com o parâmetro *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="d40d6-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="d40d6-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d40d6-134">-Name</span></span>
<span data-ttu-id="d40d6-135">Especifica um nome para o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="d40d6-136">O nome do recurso deve ser exclusivo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d40d6-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="d40d6-137">Se um grupo de recursos com esse nome já existir, o comando solicitará confirmação antes de substituir o grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d40d6-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="d40d6-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="d40d6-138">-Pre</span></span>
<span data-ttu-id="d40d6-139">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d40d6-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d40d6-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="d40d6-140">-Tag</span></span>
<span data-ttu-id="d40d6-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d40d6-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d40d6-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d40d6-142">For example:</span></span>

<span data-ttu-id="d40d6-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d40d6-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="d40d6-144">Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="d40d6-145">Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzureRmResource e Get-AzureRmResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor.</span><span class="sxs-lookup"><span data-stu-id="d40d6-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="d40d6-146">Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="d40d6-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="d40d6-147">Para obter suas marcas predefinidas, use o cmdlet Get-AzureRMTag.</span><span class="sxs-lookup"><span data-stu-id="d40d6-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="d40d6-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d40d6-148">-Confirm</span></span>
<span data-ttu-id="d40d6-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d40d6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d40d6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d40d6-150">-WhatIf</span></span>
<span data-ttu-id="d40d6-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d40d6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d40d6-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d40d6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d40d6-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40d6-153">-DefaultProfile</span></span>
<span data-ttu-id="d40d6-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d40d6-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d40d6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40d6-155">CommonParameters</span></span>
<span data-ttu-id="d40d6-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40d6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40d6-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40d6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40d6-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d40d6-158">INPUTS</span></span>

### <span data-ttu-id="d40d6-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d40d6-159">None</span></span>

## <span data-ttu-id="d40d6-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d40d6-160">OUTPUTS</span></span>

### <span data-ttu-id="d40d6-161">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d40d6-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="d40d6-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d40d6-162">NOTES</span></span>

## <span data-ttu-id="d40d6-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d40d6-163">RELATED LINKS</span></span>

[<span data-ttu-id="d40d6-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d40d6-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="d40d6-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d40d6-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="d40d6-166">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d40d6-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d40d6-167">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d40d6-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d40d6-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d40d6-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="d40d6-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d40d6-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
