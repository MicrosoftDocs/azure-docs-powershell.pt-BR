---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ce726675946b2b8dc40feb82a529ccf27ccef443
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893380"
---
# <span data-ttu-id="c48d9-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c48d9-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="c48d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c48d9-103">Obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="c48d9-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c48d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c48d9-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48d9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c48d9-105">DESCRIPTION</span></span>
<span data-ttu-id="c48d9-106">O cmdlet **Get-AzVMExtensionImage** obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="c48d9-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c48d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c48d9-107">EXAMPLES</span></span>

### <span data-ttu-id="c48d9-108">Exemplo 1: Obter as versões de uma imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="c48d9-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="c48d9-109">Este comando obtém todas as versões da imagem de extensão para o local, o editor e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="c48d9-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="c48d9-110">Exemplo 2: Obter as versões de uma imagem de extensão com filtro sobre versão</span><span class="sxs-lookup"><span data-stu-id="c48d9-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="c48d9-111">Este comando obtém todas as versões da imagem de extensão para o local, o editor, o tipo e a versão especificados a partir de 12.</span><span class="sxs-lookup"><span data-stu-id="c48d9-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="c48d9-112">Exemplo 3: Obter as versões de uma imagem de extensão com filtro sobre a versão</span><span class="sxs-lookup"><span data-stu-id="c48d9-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="c48d9-113">Este comando obtém todas as versões da imagem de extensão para o local, o editor, o tipo e a versão especificados.</span><span class="sxs-lookup"><span data-stu-id="c48d9-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="c48d9-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c48d9-114">PARAMETERS</span></span>

### <span data-ttu-id="c48d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48d9-115">-DefaultProfile</span></span>
<span data-ttu-id="c48d9-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c48d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c48d9-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c48d9-117">-FilterExpression</span></span>
<span data-ttu-id="c48d9-118">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="c48d9-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="c48d9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c48d9-119">-Location</span></span>
<span data-ttu-id="c48d9-120">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="c48d9-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="c48d9-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c48d9-121">-PublisherName</span></span>
<span data-ttu-id="c48d9-122">Especifica o nome de um editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="c48d9-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="c48d9-123">Para obter um editor de extensão, use o cmdlet Get-AzVMImagePublisher de extensão.</span><span class="sxs-lookup"><span data-stu-id="c48d9-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c48d9-124">-Type</span><span class="sxs-lookup"><span data-stu-id="c48d9-124">-Type</span></span>
<span data-ttu-id="c48d9-125">Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="c48d9-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="c48d9-126">Para obter um tipo de extensão, use o Get-AzVMExtensionImageType cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c48d9-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="c48d9-127">-Version</span><span class="sxs-lookup"><span data-stu-id="c48d9-127">-Version</span></span>
<span data-ttu-id="c48d9-128">Especifica a versão da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c48d9-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c48d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48d9-129">CommonParameters</span></span>
<span data-ttu-id="c48d9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48d9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c48d9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48d9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c48d9-132">INPUTS</span></span>

### <span data-ttu-id="c48d9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c48d9-133">System.String</span></span>

## <span data-ttu-id="c48d9-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c48d9-134">OUTPUTS</span></span>

### <span data-ttu-id="c48d9-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c48d9-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="c48d9-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="c48d9-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="c48d9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="c48d9-137">NOTES</span></span>

## <span data-ttu-id="c48d9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c48d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="c48d9-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c48d9-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="c48d9-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c48d9-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c48d9-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c48d9-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


