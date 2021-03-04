---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 983eba222959fb11a50ce94704ebdf39a9bc9fbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893377"
---
# <span data-ttu-id="3f08c-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3f08c-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="3f08c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f08c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f08c-103">Obtém os editores VMImage.</span><span class="sxs-lookup"><span data-stu-id="3f08c-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="3f08c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f08c-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f08c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f08c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f08c-106">O cmdlet **Get-AzVMImagePublisher** obtém os editores VMImage.</span><span class="sxs-lookup"><span data-stu-id="3f08c-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="3f08c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f08c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f08c-108">Exemplo 1: Obter editores VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="3f08c-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="3f08c-109">Este comando obtém os editores de instâncias do VMImage para a região central dos EUA no perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f08c-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="3f08c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f08c-110">PARAMETERS</span></span>

### <span data-ttu-id="3f08c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f08c-111">-DefaultProfile</span></span>
<span data-ttu-id="3f08c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3f08c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f08c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="3f08c-113">-Location</span></span>
<span data-ttu-id="3f08c-114">Especifica o local do VMImage.</span><span class="sxs-lookup"><span data-stu-id="3f08c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3f08c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f08c-115">CommonParameters</span></span>
<span data-ttu-id="3f08c-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f08c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f08c-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f08c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f08c-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f08c-118">INPUTS</span></span>

### <span data-ttu-id="3f08c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="3f08c-119">System.String</span></span>

## <span data-ttu-id="3f08c-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f08c-120">OUTPUTS</span></span>

### <span data-ttu-id="3f08c-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3f08c-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="3f08c-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f08c-122">NOTES</span></span>

## <span data-ttu-id="3f08c-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f08c-123">RELATED LINKS</span></span>

[<span data-ttu-id="3f08c-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3f08c-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3f08c-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3f08c-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="3f08c-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3f08c-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="3f08c-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3f08c-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


