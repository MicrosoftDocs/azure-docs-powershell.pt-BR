---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773362"
---
# <span data-ttu-id="f04a9-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f04a9-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="f04a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f04a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f04a9-103">Obtém grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="f04a9-103">Gets resource groups.</span></span>

## <span data-ttu-id="f04a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f04a9-104">SYNTAX</span></span>

### <span data-ttu-id="f04a9-105">GetByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f04a9-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f04a9-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f04a9-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f04a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f04a9-107">DESCRIPTION</span></span>
<span data-ttu-id="f04a9-108">O cmdlet **Get-AzResourceGroup** Obtém grupos de recursos do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f04a9-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="f04a9-109">Você pode obter todos os grupos de recursos ou especificar um grupo de recursos por nome ou por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="f04a9-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="f04a9-110">Por padrão, esse cmdlet obtém todos os grupos de recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f04a9-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="f04a9-111">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f04a9-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="f04a9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f04a9-112">EXAMPLES</span></span>

### <span data-ttu-id="f04a9-113">Exemplo 1: obter um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="f04a9-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="f04a9-114">Esse comando obtém o grupo de recursos do Azure na sua assinatura chamado EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="f04a9-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="f04a9-115">Exemplo 2: obter todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f04a9-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="f04a9-116">Esse comando obtém o grupo de recursos denominado ContosoRG e exibe as marcas associadas a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="f04a9-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="f04a9-117">Exemplo 3: mostrar os grupos de recursos por localização</span><span class="sxs-lookup"><span data-stu-id="f04a9-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="f04a9-118">Exemplo 4: mostrar os nomes de todos os grupos de recursos em um local específico</span><span class="sxs-lookup"><span data-stu-id="f04a9-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="f04a9-119">Exemplo 5: mostrar os grupos de recursos cujos nomes começam com o WebServer</span><span class="sxs-lookup"><span data-stu-id="f04a9-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="f04a9-120">Exemplo 6: obter um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="f04a9-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="f04a9-121">Esse comando obtém o grupo de recursos do Azure na sua assinatura que começa com "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="f04a9-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="f04a9-122">OS</span><span class="sxs-lookup"><span data-stu-id="f04a9-122">PARAMETERS</span></span>

### <span data-ttu-id="f04a9-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f04a9-123">-ApiVersion</span></span>
<span data-ttu-id="f04a9-124">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="f04a9-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f04a9-125">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="f04a9-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f04a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04a9-126">-DefaultProfile</span></span>
<span data-ttu-id="f04a9-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f04a9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f04a9-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f04a9-128">-Id</span></span>
<span data-ttu-id="f04a9-129">Especifica a ID do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="f04a9-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="f04a9-130">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="f04a9-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="f04a9-131">-Local</span><span class="sxs-lookup"><span data-stu-id="f04a9-131">-Location</span></span>
<span data-ttu-id="f04a9-132">Especifica o local do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="f04a9-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="f04a9-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="f04a9-133">-Name</span></span>
<span data-ttu-id="f04a9-134">Especifica o nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="f04a9-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="f04a9-135">Esse parâmetro dá suporte a caracteres curinga no início e/ou final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f04a9-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="f04a9-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="f04a9-136">-Pre</span></span>
<span data-ttu-id="f04a9-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f04a9-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f04a9-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="f04a9-138">-Tag</span></span>
<span data-ttu-id="f04a9-139">A Hashtable de marca para filtrar grupos de recursos por.</span><span class="sxs-lookup"><span data-stu-id="f04a9-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="f04a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04a9-140">CommonParameters</span></span>
<span data-ttu-id="f04a9-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f04a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04a9-142">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f04a9-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04a9-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f04a9-143">INPUTS</span></span>

### <span data-ttu-id="f04a9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f04a9-144">System.String</span></span>

### <span data-ttu-id="f04a9-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f04a9-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f04a9-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f04a9-146">OUTPUTS</span></span>

### <span data-ttu-id="f04a9-147">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f04a9-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="f04a9-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f04a9-148">NOTES</span></span>

## <span data-ttu-id="f04a9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f04a9-149">RELATED LINKS</span></span>

[<span data-ttu-id="f04a9-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f04a9-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="f04a9-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f04a9-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="f04a9-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f04a9-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


