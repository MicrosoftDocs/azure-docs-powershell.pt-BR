---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ebe1720154c45b08eb84cfe6c1ee4e339859e5fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597436"
---
# <span data-ttu-id="69459-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="69459-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="69459-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69459-102">SYNOPSIS</span></span>
<span data-ttu-id="69459-103">Obtém todas as versões para uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="69459-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="69459-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69459-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69459-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69459-105">DESCRIPTION</span></span>
<span data-ttu-id="69459-106">O cmdlet **Get-AzVMExtensionImage** obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="69459-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="69459-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69459-107">EXAMPLES</span></span>

### <span data-ttu-id="69459-108">Exemplo 1: obter as versões de uma imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="69459-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="69459-109">Esse comando obtém todas as versões da imagem de extensão para o local, o editor e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="69459-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="69459-110">Exemplo 2: obter as versões de uma imagem de extensão com o filtro sobre a versão</span><span class="sxs-lookup"><span data-stu-id="69459-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="69459-111">Esse comando obtém todas as versões da imagem de extensão para o local especificado, o Publisher, o tipo e a versão começando com 12.</span><span class="sxs-lookup"><span data-stu-id="69459-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="69459-112">Exemplo 3: obter as versões de uma imagem de extensão com o filtro sobre a versão</span><span class="sxs-lookup"><span data-stu-id="69459-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="69459-113">Esse comando obtém todas as versões da imagem de extensão para o local, o tipo e a versão especificados.</span><span class="sxs-lookup"><span data-stu-id="69459-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="69459-114">OS</span><span class="sxs-lookup"><span data-stu-id="69459-114">PARAMETERS</span></span>

### <span data-ttu-id="69459-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69459-115">-DefaultProfile</span></span>
<span data-ttu-id="69459-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69459-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69459-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="69459-117">-FilterExpression</span></span>
<span data-ttu-id="69459-118">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="69459-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="69459-119">-Local</span><span class="sxs-lookup"><span data-stu-id="69459-119">-Location</span></span>
<span data-ttu-id="69459-120">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="69459-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="69459-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="69459-121">-PublisherName</span></span>
<span data-ttu-id="69459-122">Especifica o nome de um fornecedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="69459-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="69459-123">Para obter um fornecedor de extensão, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="69459-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="69459-124">-Digite</span><span class="sxs-lookup"><span data-stu-id="69459-124">-Type</span></span>
<span data-ttu-id="69459-125">Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="69459-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="69459-126">Para obter um tipo de extensão, use o cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="69459-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="69459-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="69459-127">-Version</span></span>
<span data-ttu-id="69459-128">Especifica a versão da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="69459-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69459-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69459-129">CommonParameters</span></span>
<span data-ttu-id="69459-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69459-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69459-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69459-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69459-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69459-132">INPUTS</span></span>

### <span data-ttu-id="69459-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69459-133">System.String</span></span>

## <span data-ttu-id="69459-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69459-134">OUTPUTS</span></span>

### <span data-ttu-id="69459-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="69459-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="69459-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="69459-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="69459-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69459-137">NOTES</span></span>

## <span data-ttu-id="69459-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69459-138">RELATED LINKS</span></span>

[<span data-ttu-id="69459-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="69459-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="69459-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="69459-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="69459-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="69459-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


