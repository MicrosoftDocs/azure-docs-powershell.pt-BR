---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 709fab1ab8ba39193ef9831cd03d7b1cd53208dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891873"
---
# <span data-ttu-id="c7468-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c7468-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="c7468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7468-102">SYNOPSIS</span></span>
<span data-ttu-id="c7468-103">Concede acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="c7468-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="c7468-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7468-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7468-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7468-105">DESCRIPTION</span></span>
<span data-ttu-id="c7468-106">O cmdlet **Grant-AzDiskAccess** concede acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="c7468-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="c7468-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7468-107">EXAMPLES</span></span>

### <span data-ttu-id="c7468-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7468-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="c7468-109">Conceda acesso 'Leitura' ao disco chamado 'Disk01' no grupo de recursos chamado 'ResourceGroup01' por 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="c7468-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="c7468-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7468-110">PARAMETERS</span></span>

### <span data-ttu-id="c7468-111">-Access</span><span class="sxs-lookup"><span data-stu-id="c7468-111">-Access</span></span>
<span data-ttu-id="c7468-112">Especifica o nível de Acesso.</span><span class="sxs-lookup"><span data-stu-id="c7468-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7468-113">-AsJob</span></span>
<span data-ttu-id="c7468-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c7468-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7468-115">-DefaultProfile</span></span>
<span data-ttu-id="c7468-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c7468-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c7468-117">-DiskName</span></span>
<span data-ttu-id="c7468-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="c7468-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="c7468-119">-DurationInSecond</span></span>
<span data-ttu-id="c7468-120">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="c7468-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7468-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7468-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7468-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7468-123">-Confirm</span></span>
<span data-ttu-id="c7468-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7468-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7468-125">-WhatIf</span></span>
<span data-ttu-id="c7468-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7468-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7468-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7468-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7468-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7468-128">CommonParameters</span></span>
<span data-ttu-id="c7468-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7468-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7468-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7468-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7468-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7468-131">INPUTS</span></span>

### <span data-ttu-id="c7468-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c7468-132">System.String</span></span>

## <span data-ttu-id="c7468-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7468-133">OUTPUTS</span></span>

### <span data-ttu-id="c7468-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="c7468-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="c7468-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7468-135">NOTES</span></span>

## <span data-ttu-id="c7468-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7468-136">RELATED LINKS</span></span>
