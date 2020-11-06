---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427609"
---
# <span data-ttu-id="4ffea-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="4ffea-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="4ffea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ffea-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffea-103">Remove um disco.</span><span class="sxs-lookup"><span data-stu-id="4ffea-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ffea-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ffea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ffea-105">DESCRIPTION</span></span>
<span data-ttu-id="4ffea-106">O cmdlet **Remove-AzureRmDisk** remove um disco.</span><span class="sxs-lookup"><span data-stu-id="4ffea-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="4ffea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ffea-107">EXAMPLES</span></span>

### <span data-ttu-id="4ffea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ffea-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="4ffea-109">Este comando Remove o disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4ffea-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4ffea-110">OS</span><span class="sxs-lookup"><span data-stu-id="4ffea-110">PARAMETERS</span></span>

### <span data-ttu-id="4ffea-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="4ffea-111">-DiskName</span></span>
<span data-ttu-id="4ffea-112">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="4ffea-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4ffea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ffea-113">-Force</span></span>
<span data-ttu-id="4ffea-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4ffea-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffea-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ffea-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ffea-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4ffea-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ffea-117">-Confirm</span></span>
<span data-ttu-id="4ffea-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ffea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ffea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffea-119">-WhatIf</span></span>
<span data-ttu-id="4ffea-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ffea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ffea-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ffea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ffea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffea-122">CommonParameters</span></span>
<span data-ttu-id="4ffea-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffea-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffea-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ffea-125">INPUTS</span></span>

### <span data-ttu-id="4ffea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4ffea-126">System.String</span></span>

## <span data-ttu-id="4ffea-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ffea-127">OUTPUTS</span></span>

### <span data-ttu-id="4ffea-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ffea-128">System.Object</span></span>

## <span data-ttu-id="4ffea-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ffea-129">NOTES</span></span>

## <span data-ttu-id="4ffea-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ffea-130">RELATED LINKS</span></span>

