---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429863"
---
# <span data-ttu-id="71aff-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="71aff-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="71aff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71aff-102">SYNOPSIS</span></span>
<span data-ttu-id="71aff-103">Remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="71aff-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71aff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71aff-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71aff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71aff-105">DESCRIPTION</span></span>
<span data-ttu-id="71aff-106">O cmdlet **Remove-AzureRmSnapshot** remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="71aff-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="71aff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71aff-107">EXAMPLES</span></span>

### <span data-ttu-id="71aff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71aff-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="71aff-109">Este comando Remove o instantâneo chamado "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="71aff-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="71aff-110">OS</span><span class="sxs-lookup"><span data-stu-id="71aff-110">PARAMETERS</span></span>

### <span data-ttu-id="71aff-111">-Force</span><span class="sxs-lookup"><span data-stu-id="71aff-111">-Force</span></span>
<span data-ttu-id="71aff-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="71aff-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71aff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71aff-113">-ResourceGroupName</span></span>
<span data-ttu-id="71aff-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71aff-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71aff-115">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="71aff-115">-SnapshotName</span></span>
<span data-ttu-id="71aff-116">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="71aff-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="71aff-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71aff-117">-Confirm</span></span>
<span data-ttu-id="71aff-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71aff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71aff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71aff-119">-WhatIf</span></span>
<span data-ttu-id="71aff-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71aff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71aff-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71aff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71aff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71aff-122">CommonParameters</span></span>
<span data-ttu-id="71aff-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71aff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71aff-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71aff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71aff-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71aff-125">INPUTS</span></span>

### <span data-ttu-id="71aff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="71aff-126">System.String</span></span>

## <span data-ttu-id="71aff-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71aff-127">OUTPUTS</span></span>

### <span data-ttu-id="71aff-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="71aff-128">System.Object</span></span>

## <span data-ttu-id="71aff-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71aff-129">NOTES</span></span>

## <span data-ttu-id="71aff-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71aff-130">RELATED LINKS</span></span>

