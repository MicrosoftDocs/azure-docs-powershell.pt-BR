---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441610"
---
# <span data-ttu-id="605d0-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="605d0-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="605d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="605d0-102">SYNOPSIS</span></span>
<span data-ttu-id="605d0-103">Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="605d0-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="605d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="605d0-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="605d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="605d0-105">DESCRIPTION</span></span>
<span data-ttu-id="605d0-106">O cmdlet **Get-AzureRmVMImagePublisher** Obtém os editores da VMImage.</span><span class="sxs-lookup"><span data-stu-id="605d0-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="605d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="605d0-107">EXAMPLES</span></span>

### <span data-ttu-id="605d0-108">Exemplo 1: obter editores de VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="605d0-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="605d0-109">Esse comando obtém os editores de instâncias de VMImage para a região central dos EUA dentro do seu perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="605d0-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="605d0-110">OS</span><span class="sxs-lookup"><span data-stu-id="605d0-110">PARAMETERS</span></span>

### <span data-ttu-id="605d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605d0-111">-DefaultProfile</span></span>
<span data-ttu-id="605d0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="605d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="605d0-113">-Local</span><span class="sxs-lookup"><span data-stu-id="605d0-113">-Location</span></span>
<span data-ttu-id="605d0-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="605d0-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="605d0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605d0-115">CommonParameters</span></span>
<span data-ttu-id="605d0-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605d0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605d0-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605d0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605d0-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="605d0-118">INPUTS</span></span>

### <span data-ttu-id="605d0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="605d0-119">System.String</span></span>

## <span data-ttu-id="605d0-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="605d0-120">OUTPUTS</span></span>

### <span data-ttu-id="605d0-121">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="605d0-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="605d0-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="605d0-122">NOTES</span></span>

## <span data-ttu-id="605d0-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="605d0-123">RELATED LINKS</span></span>

[<span data-ttu-id="605d0-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="605d0-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="605d0-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="605d0-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="605d0-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="605d0-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="605d0-127">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="605d0-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


