---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 73defde38ab34bc81adf904d5139308dfd556f79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429376"
---
# <span data-ttu-id="9980b-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9980b-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="9980b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9980b-102">SYNOPSIS</span></span>
<span data-ttu-id="9980b-103">Obtém grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="9980b-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9980b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9980b-104">SYNTAX</span></span>

### <span data-ttu-id="9980b-105">GetByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9980b-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9980b-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9980b-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9980b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9980b-107">DESCRIPTION</span></span>
<span data-ttu-id="9980b-108">O cmdlet **Get-AzureRmResourceGroup** Obtém grupos de recursos do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9980b-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="9980b-109">Você pode obter todos os grupos de recursos ou especificar um grupo de recursos por nome ou por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="9980b-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="9980b-110">Por padrão, esse cmdlet obtém todos os grupos de recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9980b-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="9980b-111">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9980b-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="9980b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9980b-112">EXAMPLES</span></span>

### <span data-ttu-id="9980b-113">Exemplo 1: obter um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="9980b-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="9980b-114">Esse comando obtém o grupo de recursos do Azure na sua assinatura chamado EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="9980b-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="9980b-115">Exemplo 2: obter todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9980b-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="9980b-116">Esse comando obtém o grupo de recursos denominado ContosoRG e exibe as marcas associadas a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="9980b-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="9980b-117">Exemplo 3: mostrar os grupos de recursos por localização</span><span class="sxs-lookup"><span data-stu-id="9980b-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="9980b-118">Exemplo 4: mostrar os nomes de todos os grupos de recursos em um local específico</span><span class="sxs-lookup"><span data-stu-id="9980b-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="9980b-119">Exemplo 5: mostrar os grupos de recursos cujos nomes começam com o WebServer</span><span class="sxs-lookup"><span data-stu-id="9980b-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="9980b-120">OS</span><span class="sxs-lookup"><span data-stu-id="9980b-120">PARAMETERS</span></span>

### <span data-ttu-id="9980b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9980b-121">-ApiVersion</span></span>
<span data-ttu-id="9980b-122">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="9980b-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9980b-123">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="9980b-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9980b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9980b-124">-DefaultProfile</span></span>
<span data-ttu-id="9980b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9980b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9980b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="9980b-126">-Id</span></span>
<span data-ttu-id="9980b-127">Especifica a ID do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="9980b-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="9980b-128">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="9980b-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="9980b-129">-Local</span><span class="sxs-lookup"><span data-stu-id="9980b-129">-Location</span></span>
<span data-ttu-id="9980b-130">Especifica o local do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="9980b-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9980b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="9980b-131">-Name</span></span>
<span data-ttu-id="9980b-132">Especifica o nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9980b-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="9980b-133">Esse parâmetro dá suporte a caracteres curinga no início e/ou final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9980b-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9980b-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="9980b-134">-Pre</span></span>
<span data-ttu-id="9980b-135">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9980b-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9980b-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="9980b-136">-Tag</span></span>
<span data-ttu-id="9980b-137">A Hashtable de marca para filtrar grupos de recursos por.</span><span class="sxs-lookup"><span data-stu-id="9980b-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="9980b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9980b-138">CommonParameters</span></span>
<span data-ttu-id="9980b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9980b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9980b-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9980b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9980b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9980b-141">INPUTS</span></span>

### <span data-ttu-id="9980b-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9980b-142">None</span></span>

## <span data-ttu-id="9980b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9980b-143">OUTPUTS</span></span>

### <span data-ttu-id="9980b-144">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9980b-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="9980b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9980b-145">NOTES</span></span>

## <span data-ttu-id="9980b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9980b-146">RELATED LINKS</span></span>

[<span data-ttu-id="9980b-147">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9980b-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="9980b-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9980b-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="9980b-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9980b-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


