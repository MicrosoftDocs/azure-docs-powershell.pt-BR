---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440500"
---
# <span data-ttu-id="18c82-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="18c82-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="18c82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18c82-102">SYNOPSIS</span></span>
<span data-ttu-id="18c82-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="18c82-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18c82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18c82-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18c82-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18c82-105">DESCRIPTION</span></span>
<span data-ttu-id="18c82-106">O cmdlet **REVOKE-AzureRmDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="18c82-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="18c82-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18c82-107">EXAMPLES</span></span>

### <span data-ttu-id="18c82-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18c82-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="18c82-109">Revogue o acesso ao disco chamado ' Disk01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="18c82-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="18c82-110">OS</span><span class="sxs-lookup"><span data-stu-id="18c82-110">PARAMETERS</span></span>

### <span data-ttu-id="18c82-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="18c82-111">-DiskName</span></span>
<span data-ttu-id="18c82-112">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="18c82-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="18c82-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c82-113">-ResourceGroupName</span></span>
<span data-ttu-id="18c82-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18c82-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18c82-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18c82-115">-Confirm</span></span>
<span data-ttu-id="18c82-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c82-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c82-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c82-117">-WhatIf</span></span>
<span data-ttu-id="18c82-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18c82-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18c82-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18c82-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c82-120">CommonParameters</span></span>
<span data-ttu-id="18c82-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c82-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c82-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18c82-123">INPUTS</span></span>

### <span data-ttu-id="18c82-124">System. String</span><span class="sxs-lookup"><span data-stu-id="18c82-124">System.String</span></span>

## <span data-ttu-id="18c82-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18c82-125">OUTPUTS</span></span>

### <span data-ttu-id="18c82-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="18c82-126">System.Object</span></span>

## <span data-ttu-id="18c82-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18c82-127">NOTES</span></span>

## <span data-ttu-id="18c82-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18c82-128">RELATED LINKS</span></span>

