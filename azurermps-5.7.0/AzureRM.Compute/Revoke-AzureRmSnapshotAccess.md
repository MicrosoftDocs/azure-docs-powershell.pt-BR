---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610410"
---
# <span data-ttu-id="b1daf-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b1daf-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="b1daf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1daf-102">SYNOPSIS</span></span>
<span data-ttu-id="b1daf-103">Revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b1daf-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1daf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1daf-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1daf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1daf-105">DESCRIPTION</span></span>
<span data-ttu-id="b1daf-106">O cmdlet **REVOKE-AzureRmSnapshotAccess** revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b1daf-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="b1daf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1daf-107">EXAMPLES</span></span>

### <span data-ttu-id="b1daf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1daf-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="b1daf-109">Revogue o acesso ao instantâneo chamado ' Snapshot01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="b1daf-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="b1daf-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1daf-110">PARAMETERS</span></span>

### <span data-ttu-id="b1daf-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1daf-111">-ResourceGroupName</span></span>
<span data-ttu-id="b1daf-112">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1daf-112">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-113">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="b1daf-113">-SnapshotName</span></span>
<span data-ttu-id="b1daf-114">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b1daf-114">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1daf-115">-Confirm</span></span>
<span data-ttu-id="b1daf-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1daf-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1daf-117">-WhatIf</span></span>
<span data-ttu-id="b1daf-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1daf-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1daf-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1daf-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1daf-120">CommonParameters</span></span>
<span data-ttu-id="b1daf-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1daf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1daf-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1daf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1daf-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1daf-123">INPUTS</span></span>

### <span data-ttu-id="b1daf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b1daf-124">System.String</span></span>

## <span data-ttu-id="b1daf-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1daf-125">OUTPUTS</span></span>

### <span data-ttu-id="b1daf-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="b1daf-126">System.Object</span></span>

## <span data-ttu-id="b1daf-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1daf-127">NOTES</span></span>

## <span data-ttu-id="b1daf-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1daf-128">RELATED LINKS</span></span>

