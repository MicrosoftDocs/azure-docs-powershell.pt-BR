---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440688"
---
# <span data-ttu-id="81329-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="81329-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="81329-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81329-102">SYNOPSIS</span></span>
<span data-ttu-id="81329-103">Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="81329-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81329-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81329-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81329-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81329-105">DESCRIPTION</span></span>
<span data-ttu-id="81329-106">O cmdlet **Get-AzureRmVMImagePublisher** Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="81329-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="81329-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81329-107">EXAMPLES</span></span>

### <span data-ttu-id="81329-108">Exemplo 1: obter editores de VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="81329-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="81329-109">Esse comando obtém os editores de instâncias de VMImage para a região central dos EUA dentro do seu perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="81329-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="81329-110">OS</span><span class="sxs-lookup"><span data-stu-id="81329-110">PARAMETERS</span></span>

### <span data-ttu-id="81329-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81329-111">-DefaultProfile</span></span>
<span data-ttu-id="81329-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81329-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81329-113">-Local</span><span class="sxs-lookup"><span data-stu-id="81329-113">-Location</span></span>
<span data-ttu-id="81329-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="81329-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="81329-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81329-115">CommonParameters</span></span>
<span data-ttu-id="81329-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81329-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81329-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81329-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81329-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81329-118">INPUTS</span></span>

## <span data-ttu-id="81329-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81329-119">OUTPUTS</span></span>

## <span data-ttu-id="81329-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81329-120">NOTES</span></span>

## <span data-ttu-id="81329-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81329-121">RELATED LINKS</span></span>

[<span data-ttu-id="81329-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="81329-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="81329-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="81329-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="81329-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="81329-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="81329-125">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="81329-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


