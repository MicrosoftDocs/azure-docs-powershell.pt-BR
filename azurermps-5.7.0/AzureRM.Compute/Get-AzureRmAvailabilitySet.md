---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431075"
---
# <span data-ttu-id="3344d-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3344d-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="3344d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3344d-102">SYNOPSIS</span></span>
<span data-ttu-id="3344d-103">Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3344d-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3344d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3344d-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="3344d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3344d-105">DESCRIPTION</span></span>
<span data-ttu-id="3344d-106">O cmdlet **Get-AzureRmAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3344d-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="3344d-107">Você pode especificar o nome de um conjunto de disponibilidade específico para obter.</span><span class="sxs-lookup"><span data-stu-id="3344d-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="3344d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3344d-108">EXAMPLES</span></span>

### <span data-ttu-id="3344d-109">Exemplo 1: obter um conjunto de disponibilidade específico</span><span class="sxs-lookup"><span data-stu-id="3344d-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="3344d-110">Esse comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3344d-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="3344d-111">Exemplo 2: obter todos os conjuntos de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3344d-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3344d-112">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3344d-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3344d-113">OS</span><span class="sxs-lookup"><span data-stu-id="3344d-113">PARAMETERS</span></span>

### <span data-ttu-id="3344d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3344d-114">-Name</span></span>
<span data-ttu-id="3344d-115">Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="3344d-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3344d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3344d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3344d-117">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3344d-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3344d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3344d-118">CommonParameters</span></span>
<span data-ttu-id="3344d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3344d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3344d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3344d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3344d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3344d-121">INPUTS</span></span>

### <span data-ttu-id="3344d-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3344d-122">None</span></span>
<span data-ttu-id="3344d-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3344d-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3344d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3344d-124">OUTPUTS</span></span>

## <span data-ttu-id="3344d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3344d-125">NOTES</span></span>

## <span data-ttu-id="3344d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3344d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3344d-127">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3344d-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="3344d-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3344d-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


