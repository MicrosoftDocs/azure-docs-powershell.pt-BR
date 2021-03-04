---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: e431e1e9186cdaf0ec722b5a609a3f0a9f186bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888078"
---
# <span data-ttu-id="4eb7a-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4eb7a-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="4eb7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb7a-103">Obtém grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-103">Gets resource groups.</span></span>

## <span data-ttu-id="4eb7a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4eb7a-104">SYNTAX</span></span>

### <span data-ttu-id="4eb7a-105">GetByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4eb7a-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb7a-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4eb7a-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb7a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4eb7a-107">DESCRIPTION</span></span>
<span data-ttu-id="4eb7a-108">O cmdlet **Get-AzResourceGroup** obtém grupos de recursos do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="4eb7a-109">Você pode obter todos os grupos de recursos ou especificar um grupo de recursos pelo nome ou por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="4eb7a-110">Por padrão, esse cmdlet obtém todos os grupos de recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="4eb7a-111">Para obter mais informações sobre recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="4eb7a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-112">EXAMPLES</span></span>

### <span data-ttu-id="4eb7a-113">Exemplo 1: Obter um grupo de recursos pelo nome</span><span class="sxs-lookup"><span data-stu-id="4eb7a-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="4eb7a-114">Este comando obtém o grupo de recursos do Azure em sua assinatura chamada EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="4eb7a-115">Exemplo 2: Obter todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4eb7a-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="4eb7a-116">Este comando obtém o grupo de recursos chamado ContosoRG e exibe as marcas associadas a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="4eb7a-117">Exemplo 3: Obter grupos de recursos com base na marca</span><span class="sxs-lookup"><span data-stu-id="4eb7a-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="4eb7a-118">Exemplo 4: Mostrar os grupos de recursos por local</span><span class="sxs-lookup"><span data-stu-id="4eb7a-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="4eb7a-119">Exemplo 5: Mostrar os nomes de todos os grupos de recursos em um local específico</span><span class="sxs-lookup"><span data-stu-id="4eb7a-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="4eb7a-120">Exemplo 6: Mostrar os grupos de recursos cujos nomes começam com o WebServer</span><span class="sxs-lookup"><span data-stu-id="4eb7a-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="4eb7a-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-121">PARAMETERS</span></span>

### <span data-ttu-id="4eb7a-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4eb7a-122">-ApiVersion</span></span>
<span data-ttu-id="4eb7a-123">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4eb7a-124">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4eb7a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb7a-125">-DefaultProfile</span></span>
<span data-ttu-id="4eb7a-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4eb7a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb7a-127">-Id</span><span class="sxs-lookup"><span data-stu-id="4eb7a-127">-Id</span></span>
<span data-ttu-id="4eb7a-128">Especifica a ID do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="4eb7a-129">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb7a-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4eb7a-130">-Location</span></span>
<span data-ttu-id="4eb7a-131">Especifica o local do grupo de recursos a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb7a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb7a-132">-Name</span></span>
<span data-ttu-id="4eb7a-133">Especifica o nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="4eb7a-134">Este parâmetro dá suporte a caracteres curinga no início e/ou no final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4eb7a-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="4eb7a-135">-Pre</span></span>
<span data-ttu-id="4eb7a-136">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4eb7a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="4eb7a-137">-Tag</span></span>
<span data-ttu-id="4eb7a-138">A hashtable de marca para filtrar grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb7a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb7a-139">CommonParameters</span></span>
<span data-ttu-id="4eb7a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb7a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb7a-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eb7a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb7a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-142">INPUTS</span></span>

### <span data-ttu-id="4eb7a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb7a-143">System.String</span></span>

### <span data-ttu-id="4eb7a-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4eb7a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4eb7a-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-145">OUTPUTS</span></span>

### <span data-ttu-id="4eb7a-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4eb7a-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="4eb7a-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="4eb7a-147">NOTES</span></span>

## <span data-ttu-id="4eb7a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eb7a-148">RELATED LINKS</span></span>

[<span data-ttu-id="4eb7a-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4eb7a-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4eb7a-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4eb7a-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="4eb7a-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4eb7a-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

