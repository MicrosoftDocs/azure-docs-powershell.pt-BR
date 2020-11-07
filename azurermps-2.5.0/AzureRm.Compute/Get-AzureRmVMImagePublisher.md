---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786185"
---
# <span data-ttu-id="2d118-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2d118-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="2d118-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d118-102">SYNOPSIS</span></span>
<span data-ttu-id="2d118-103">Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2d118-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d118-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d118-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d118-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d118-105">DESCRIPTION</span></span>
<span data-ttu-id="2d118-106">O cmdlet **Get-AzureRmVMImagePublisher** Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2d118-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="2d118-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d118-107">EXAMPLES</span></span>

### <span data-ttu-id="2d118-108">Exemplo 1: obter editores de VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="2d118-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="2d118-109">Esse comando obtém os editores de instâncias de VMImage para a região central dos EUA dentro do seu perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d118-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="2d118-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d118-110">PARAMETERS</span></span>

### <span data-ttu-id="2d118-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d118-111">-DefaultProfile</span></span>
<span data-ttu-id="2d118-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d118-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d118-113">-Local</span><span class="sxs-lookup"><span data-stu-id="2d118-113">-Location</span></span>
<span data-ttu-id="2d118-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2d118-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d118-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d118-115">CommonParameters</span></span>
<span data-ttu-id="2d118-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d118-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d118-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d118-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d118-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d118-118">INPUTS</span></span>

### <span data-ttu-id="2d118-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2d118-119">None</span></span>
<span data-ttu-id="2d118-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2d118-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d118-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d118-121">OUTPUTS</span></span>

### <span data-ttu-id="2d118-122">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2d118-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="2d118-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d118-123">NOTES</span></span>

## <span data-ttu-id="2d118-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d118-124">RELATED LINKS</span></span>

[<span data-ttu-id="2d118-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2d118-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="2d118-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2d118-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="2d118-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2d118-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2d118-128">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2d118-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


