---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885485"
---
# <span data-ttu-id="67a1e-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="67a1e-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="67a1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="67a1e-103">Revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="67a1e-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="67a1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67a1e-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="67a1e-106">O cmdlet **Revoke-AzSnapshotAccess** revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="67a1e-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="67a1e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67a1e-107">EXAMPLES</span></span>

### <span data-ttu-id="67a1e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67a1e-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="67a1e-109">Revogar o acesso ao instantâneo chamado 'Instantâneo01' no grupo de recursos chamado 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="67a1e-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="67a1e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67a1e-110">PARAMETERS</span></span>

### <span data-ttu-id="67a1e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67a1e-111">-AsJob</span></span>
<span data-ttu-id="67a1e-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="67a1e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67a1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a1e-113">-DefaultProfile</span></span>
<span data-ttu-id="67a1e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="67a1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="67a1e-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67a1e-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67a1e-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="67a1e-117">-SnapshotName</span></span>
<span data-ttu-id="67a1e-118">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="67a1e-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="67a1e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67a1e-119">-Confirm</span></span>
<span data-ttu-id="67a1e-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a1e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a1e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a1e-121">-WhatIf</span></span>
<span data-ttu-id="67a1e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67a1e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67a1e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67a1e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a1e-124">CommonParameters</span></span>
<span data-ttu-id="67a1e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a1e-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67a1e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a1e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67a1e-127">INPUTS</span></span>

### <span data-ttu-id="67a1e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67a1e-128">System.String</span></span>

## <span data-ttu-id="67a1e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67a1e-129">OUTPUTS</span></span>

### <span data-ttu-id="67a1e-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="67a1e-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="67a1e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="67a1e-131">NOTES</span></span>

## <span data-ttu-id="67a1e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67a1e-132">RELATED LINKS</span></span>
