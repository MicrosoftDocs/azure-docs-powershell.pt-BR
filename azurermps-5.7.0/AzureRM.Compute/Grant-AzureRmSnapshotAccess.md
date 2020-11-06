---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426804"
---
# <span data-ttu-id="2da44-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2da44-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="2da44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2da44-102">SYNOPSIS</span></span>
<span data-ttu-id="2da44-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2da44-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2da44-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2da44-105">DESCRIPTION</span></span>
<span data-ttu-id="2da44-106">O cmdlet **Grant-AzureRmSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2da44-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="2da44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2da44-107">EXAMPLES</span></span>

### <span data-ttu-id="2da44-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2da44-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="2da44-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="2da44-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="2da44-110">OS</span><span class="sxs-lookup"><span data-stu-id="2da44-110">PARAMETERS</span></span>

### <span data-ttu-id="2da44-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="2da44-111">-Access</span></span>
<span data-ttu-id="2da44-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="2da44-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da44-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="2da44-113">-DurationInSecond</span></span>
<span data-ttu-id="2da44-114">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="2da44-114">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da44-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da44-115">-ResourceGroupName</span></span>
<span data-ttu-id="2da44-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2da44-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2da44-117">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="2da44-117">-SnapshotName</span></span>
<span data-ttu-id="2da44-118">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2da44-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="2da44-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2da44-119">-Confirm</span></span>
<span data-ttu-id="2da44-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da44-121">-WhatIf</span></span>
<span data-ttu-id="2da44-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2da44-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2da44-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2da44-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da44-124">CommonParameters</span></span>
<span data-ttu-id="2da44-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da44-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da44-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2da44-127">INPUTS</span></span>

### <span data-ttu-id="2da44-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2da44-128">System.String</span></span>

## <span data-ttu-id="2da44-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2da44-129">OUTPUTS</span></span>

### <span data-ttu-id="2da44-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="2da44-130">System.Object</span></span>

## <span data-ttu-id="2da44-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2da44-131">NOTES</span></span>

## <span data-ttu-id="2da44-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2da44-132">RELATED LINKS</span></span>

