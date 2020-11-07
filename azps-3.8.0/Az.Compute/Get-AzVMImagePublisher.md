---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942883"
---
# <span data-ttu-id="ae10b-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ae10b-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="ae10b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae10b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae10b-103">Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="ae10b-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="ae10b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae10b-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae10b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae10b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae10b-106">O cmdlet **Get-AzVMImagePublisher** Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="ae10b-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="ae10b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae10b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae10b-108">Exemplo 1: obter editores de VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="ae10b-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="ae10b-109">Esse comando obtém os editores de instâncias de VMImage para a região central dos EUA dentro do seu perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae10b-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="ae10b-110">OS</span><span class="sxs-lookup"><span data-stu-id="ae10b-110">PARAMETERS</span></span>

### <span data-ttu-id="ae10b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae10b-111">-DefaultProfile</span></span>
<span data-ttu-id="ae10b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae10b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae10b-113">-Local</span><span class="sxs-lookup"><span data-stu-id="ae10b-113">-Location</span></span>
<span data-ttu-id="ae10b-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="ae10b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="ae10b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae10b-115">CommonParameters</span></span>
<span data-ttu-id="ae10b-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae10b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae10b-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae10b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae10b-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae10b-118">INPUTS</span></span>

### <span data-ttu-id="ae10b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ae10b-119">System.String</span></span>

## <span data-ttu-id="ae10b-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae10b-120">OUTPUTS</span></span>

### <span data-ttu-id="ae10b-121">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ae10b-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="ae10b-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae10b-122">NOTES</span></span>

## <span data-ttu-id="ae10b-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae10b-123">RELATED LINKS</span></span>

[<span data-ttu-id="ae10b-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ae10b-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ae10b-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ae10b-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="ae10b-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ae10b-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ae10b-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ae10b-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


