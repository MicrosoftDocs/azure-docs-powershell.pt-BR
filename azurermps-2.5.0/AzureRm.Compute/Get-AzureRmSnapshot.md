---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785560"
---
# <span data-ttu-id="25bc3-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="25bc3-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="25bc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="25bc3-103">Obtém as propriedades de um instantâneo</span><span class="sxs-lookup"><span data-stu-id="25bc3-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25bc3-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25bc3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="25bc3-106">O cmdlet **Get-AzureRmSnapshot** Obtém as propriedades de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="25bc3-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="25bc3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="25bc3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25bc3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="25bc3-109">Este comando obtém as propriedades de todos os instantâneos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="25bc3-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="25bc3-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25bc3-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="25bc3-111">Esse comando obtém as propriedades de todos os instantâneos no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="25bc3-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="25bc3-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="25bc3-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="25bc3-113">Este comando obtém as propriedades do instantâneo chamado "SnapshotName1" no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="25bc3-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="25bc3-114">OS</span><span class="sxs-lookup"><span data-stu-id="25bc3-114">PARAMETERS</span></span>

### <span data-ttu-id="25bc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bc3-115">-DefaultProfile</span></span>
<span data-ttu-id="25bc3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25bc3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25bc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="25bc3-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25bc3-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25bc3-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="25bc3-119">-SnapshotName</span></span>
<span data-ttu-id="25bc3-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="25bc3-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="25bc3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bc3-121">CommonParameters</span></span>
<span data-ttu-id="25bc3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bc3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bc3-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bc3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bc3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25bc3-124">INPUTS</span></span>

### <span data-ttu-id="25bc3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="25bc3-125">System.String</span></span>

## <span data-ttu-id="25bc3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25bc3-126">OUTPUTS</span></span>

### <span data-ttu-id="25bc3-127">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="25bc3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="25bc3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25bc3-128">NOTES</span></span>

## <span data-ttu-id="25bc3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25bc3-129">RELATED LINKS</span></span>

