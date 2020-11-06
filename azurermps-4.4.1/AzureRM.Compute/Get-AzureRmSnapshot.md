---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428269"
---
# <span data-ttu-id="7c46f-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="7c46f-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="7c46f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c46f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c46f-103">Obtém as propriedades de um instantâneo</span><span class="sxs-lookup"><span data-stu-id="7c46f-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c46f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c46f-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c46f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c46f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c46f-106">O cmdlet **Get-AzureRmSnapshot** Obtém as propriedades de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7c46f-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="7c46f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c46f-107">EXAMPLES</span></span>

### <span data-ttu-id="7c46f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c46f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="7c46f-109">Este comando obtém as propriedades de todos os instantâneos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7c46f-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="7c46f-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7c46f-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="7c46f-111">Esse comando obtém as propriedades de todos os instantâneos no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="7c46f-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="7c46f-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7c46f-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="7c46f-113">Este comando obtém as propriedades do instantâneo chamado "SnapshotName1" no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="7c46f-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="7c46f-114">OS</span><span class="sxs-lookup"><span data-stu-id="7c46f-114">PARAMETERS</span></span>

### <span data-ttu-id="7c46f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c46f-115">-DefaultProfile</span></span>
<span data-ttu-id="7c46f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c46f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c46f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c46f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c46f-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c46f-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c46f-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="7c46f-119">-SnapshotName</span></span>
<span data-ttu-id="7c46f-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7c46f-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c46f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c46f-121">CommonParameters</span></span>
<span data-ttu-id="7c46f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c46f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c46f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c46f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c46f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c46f-124">INPUTS</span></span>

### <span data-ttu-id="7c46f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7c46f-125">System.String</span></span>

## <span data-ttu-id="7c46f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c46f-126">OUTPUTS</span></span>

### <span data-ttu-id="7c46f-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="7c46f-127">System.Object</span></span>

## <span data-ttu-id="7c46f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c46f-128">NOTES</span></span>

## <span data-ttu-id="7c46f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c46f-129">RELATED LINKS</span></span>

