---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610417"
---
# <span data-ttu-id="2b4de-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="2b4de-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="2b4de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b4de-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4de-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="2b4de-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b4de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b4de-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="2b4de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b4de-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4de-106">O cmdlet **Get-AzureRmVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="2b4de-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="2b4de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b4de-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4de-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="2b4de-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="2b4de-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2b4de-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="2b4de-110">OS</span><span class="sxs-lookup"><span data-stu-id="2b4de-110">PARAMETERS</span></span>

### <span data-ttu-id="2b4de-111">-Local</span><span class="sxs-lookup"><span data-stu-id="2b4de-111">-Location</span></span>
<span data-ttu-id="2b4de-112">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2b4de-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4de-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4de-113">CommonParameters</span></span>
<span data-ttu-id="2b4de-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4de-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4de-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b4de-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4de-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b4de-116">INPUTS</span></span>

### <span data-ttu-id="2b4de-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2b4de-117">None</span></span>
<span data-ttu-id="2b4de-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2b4de-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b4de-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b4de-119">OUTPUTS</span></span>

## <span data-ttu-id="2b4de-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b4de-120">NOTES</span></span>

## <span data-ttu-id="2b4de-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b4de-121">RELATED LINKS</span></span>

[<span data-ttu-id="2b4de-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b4de-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


