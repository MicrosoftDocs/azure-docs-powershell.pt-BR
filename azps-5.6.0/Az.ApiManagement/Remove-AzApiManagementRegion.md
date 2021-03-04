---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892908"
---
# <span data-ttu-id="8b041-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8b041-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="8b041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b041-102">SYNOPSIS</span></span>
<span data-ttu-id="8b041-103">Remove uma região de implantação existente da instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8b041-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="8b041-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8b041-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b041-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8b041-105">DESCRIPTION</span></span>
<span data-ttu-id="8b041-106">O cmdlet **Remove-AzApiManagementRegion** remove instância do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** de uma coleção **de AdditionalRegions** do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="8b041-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="8b041-107">Este cmdlet não modifica a implantação por si só, mas atualiza a instância **de PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="8b041-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="8b041-108">Para atualizar uma implantação de um Gerenciamento de API, passe o **PsApiManagementInstance** modificado para **Set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="8b041-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="8b041-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b041-109">EXAMPLES</span></span>

### <span data-ttu-id="8b041-110">Exemplo 1: Remover uma região de uma instância PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b041-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="8b041-111">Este comando remove a região chamada East US da **instância PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="8b041-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="8b041-112">Exemplo 2: Remover uma região de uma instância PsApiManagement usando uma série de comandos</span><span class="sxs-lookup"><span data-stu-id="8b041-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="8b041-113">Este primeiro comando obtém uma instância **de PsApiManagement** do grupo de recursos chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="8b041-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="8b041-114">Em seguida, o comando final remove a região chamada Leste dos EUA dessa instância e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="8b041-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="8b041-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8b041-115">PARAMETERS</span></span>

### <span data-ttu-id="8b041-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b041-116">-ApiManagement</span></span>
<span data-ttu-id="8b041-117">Especifica a **instância PsApiManagement** da onde esse cmdlet remove a região de implantação adicional.</span><span class="sxs-lookup"><span data-stu-id="8b041-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b041-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b041-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="8b041-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8b041-119">-Location</span></span>
<span data-ttu-id="8b041-120">Especifica o local da região que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="8b041-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="8b041-121">Especifica o local da nova região de implantação entre a região suportada para o serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="8b041-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="8b041-122">Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais</span><span class="sxs-lookup"><span data-stu-id="8b041-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8b041-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b041-123">CommonParameters</span></span>
<span data-ttu-id="8b041-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b041-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b041-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b041-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b041-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b041-126">INPUTS</span></span>

### <span data-ttu-id="8b041-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b041-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="8b041-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8b041-128">System.String</span></span>

## <span data-ttu-id="8b041-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8b041-129">OUTPUTS</span></span>

### <span data-ttu-id="8b041-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b041-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8b041-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="8b041-131">NOTES</span></span>

## <span data-ttu-id="8b041-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b041-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b041-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8b041-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="8b041-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8b041-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


