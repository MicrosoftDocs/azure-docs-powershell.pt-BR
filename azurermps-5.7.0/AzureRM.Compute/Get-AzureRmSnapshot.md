---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431064"
---
# <span data-ttu-id="22025-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="22025-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="22025-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22025-102">SYNOPSIS</span></span>
<span data-ttu-id="22025-103">Obtém as propriedades de um instantâneo</span><span class="sxs-lookup"><span data-stu-id="22025-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22025-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22025-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="22025-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22025-105">DESCRIPTION</span></span>
<span data-ttu-id="22025-106">O cmdlet **Get-AzureRmSnapshot** Obtém as propriedades de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="22025-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="22025-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22025-107">EXAMPLES</span></span>

### <span data-ttu-id="22025-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22025-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="22025-109">Este comando obtém as propriedades de todos os instantâneos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="22025-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="22025-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22025-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="22025-111">Esse comando obtém as propriedades de todos os instantâneos no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="22025-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="22025-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="22025-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="22025-113">Este comando obtém as propriedades do instantâneo chamado "SnapshotName1" no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="22025-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="22025-114">OS</span><span class="sxs-lookup"><span data-stu-id="22025-114">PARAMETERS</span></span>

### <span data-ttu-id="22025-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22025-115">-ResourceGroupName</span></span>
<span data-ttu-id="22025-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22025-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22025-117">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="22025-117">-SnapshotName</span></span>
<span data-ttu-id="22025-118">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="22025-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22025-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22025-119">CommonParameters</span></span>
<span data-ttu-id="22025-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22025-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22025-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22025-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22025-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22025-122">INPUTS</span></span>

### <span data-ttu-id="22025-123">System. String</span><span class="sxs-lookup"><span data-stu-id="22025-123">System.String</span></span>

## <span data-ttu-id="22025-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22025-124">OUTPUTS</span></span>

### <span data-ttu-id="22025-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="22025-125">System.Object</span></span>

## <span data-ttu-id="22025-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22025-126">NOTES</span></span>

## <span data-ttu-id="22025-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22025-127">RELATED LINKS</span></span>

