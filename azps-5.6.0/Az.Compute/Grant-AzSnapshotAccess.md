---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891871"
---
# <span data-ttu-id="416e4-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="416e4-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="416e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="416e4-102">SYNOPSIS</span></span>
<span data-ttu-id="416e4-103">Concede acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="416e4-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="416e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="416e4-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="416e4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="416e4-105">DESCRIPTION</span></span>
<span data-ttu-id="416e4-106">O cmdlet **Grant-AzSnapshotAccess** concede acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="416e4-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="416e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="416e4-107">EXAMPLES</span></span>

### <span data-ttu-id="416e4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="416e4-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="416e4-109">Conceda acesso 'Leitura' ao instantâneo chamado 'Instantâneo01' no grupo de recursos chamado 'ResourceGroup01' por 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="416e4-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="416e4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="416e4-110">PARAMETERS</span></span>

### <span data-ttu-id="416e4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="416e4-111">-Access</span></span>
<span data-ttu-id="416e4-112">Especifica o nível de Acesso.</span><span class="sxs-lookup"><span data-stu-id="416e4-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="416e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="416e4-113">-AsJob</span></span>
<span data-ttu-id="416e4-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="416e4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="416e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="416e4-115">-DefaultProfile</span></span>
<span data-ttu-id="416e4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="416e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="416e4-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="416e4-117">-DurationInSecond</span></span>
<span data-ttu-id="416e4-118">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="416e4-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="416e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="416e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="416e4-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="416e4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="416e4-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="416e4-121">-SnapshotName</span></span>
<span data-ttu-id="416e4-122">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="416e4-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="416e4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="416e4-123">-Confirm</span></span>
<span data-ttu-id="416e4-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="416e4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="416e4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="416e4-125">-WhatIf</span></span>
<span data-ttu-id="416e4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="416e4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="416e4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="416e4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="416e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="416e4-128">CommonParameters</span></span>
<span data-ttu-id="416e4-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="416e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="416e4-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="416e4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="416e4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="416e4-131">INPUTS</span></span>

### <span data-ttu-id="416e4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="416e4-132">System.String</span></span>

## <span data-ttu-id="416e4-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="416e4-133">OUTPUTS</span></span>

### <span data-ttu-id="416e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="416e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="416e4-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="416e4-135">NOTES</span></span>

## <span data-ttu-id="416e4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="416e4-136">RELATED LINKS</span></span>
