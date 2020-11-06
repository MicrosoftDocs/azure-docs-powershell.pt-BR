---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597967"
---
# <span data-ttu-id="14cc2-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="14cc2-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="14cc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="14cc2-103">Remove uma região de implantação existente da instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="14cc2-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="14cc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14cc2-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14cc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="14cc2-106">O cmdlet **Remove-AzApiManagementRegion** remove a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** de uma coleção de **AdditionalRegions** da fornecida a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="14cc2-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="14cc2-107">Esse cmdlet não modifica a implantação sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="14cc2-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="14cc2-108">Para atualizar uma implantação de um gerenciamento de API, passe o **PsApiManagementInstance** modificado para **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="14cc2-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="14cc2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14cc2-109">EXAMPLES</span></span>

### <span data-ttu-id="14cc2-110">Exemplo 1: remover uma região de uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="14cc2-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="14cc2-111">Esse comando Remove a região chamada leste US da instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="14cc2-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="14cc2-112">Exemplo 2: remover uma região de uma instância do PsApiManagement usando uma série de comandos</span><span class="sxs-lookup"><span data-stu-id="14cc2-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="14cc2-113">Esse primeiro comando obtém uma instância de **PsApiManagement** do grupo de recursos chamado contoso chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="14cc2-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="14cc2-114">Em seguida, o comando final remove a região chamada leste dos EUA dessa instância e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="14cc2-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="14cc2-115">OS</span><span class="sxs-lookup"><span data-stu-id="14cc2-115">PARAMETERS</span></span>

### <span data-ttu-id="14cc2-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="14cc2-116">-ApiManagement</span></span>
<span data-ttu-id="14cc2-117">Especifica a instância **PsApiManagement** para a qual esse cmdlet Remove a região de implantação adicional.</span><span class="sxs-lookup"><span data-stu-id="14cc2-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="14cc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cc2-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="14cc2-119">-Local</span><span class="sxs-lookup"><span data-stu-id="14cc2-119">-Location</span></span>
<span data-ttu-id="14cc2-120">Especifica o local da região que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="14cc2-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="14cc2-121">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="14cc2-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="14cc2-122">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="14cc2-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="14cc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cc2-123">CommonParameters</span></span>
<span data-ttu-id="14cc2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cc2-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14cc2-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cc2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14cc2-126">INPUTS</span></span>

### <span data-ttu-id="14cc2-127">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="14cc2-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="14cc2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14cc2-128">System.String</span></span>

## <span data-ttu-id="14cc2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14cc2-129">OUTPUTS</span></span>

### <span data-ttu-id="14cc2-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="14cc2-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="14cc2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14cc2-131">NOTES</span></span>

## <span data-ttu-id="14cc2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14cc2-132">RELATED LINKS</span></span>

[<span data-ttu-id="14cc2-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="14cc2-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="14cc2-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="14cc2-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


