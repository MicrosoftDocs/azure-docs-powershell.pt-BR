---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258973"
---
# <span data-ttu-id="33417-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="33417-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="33417-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33417-102">SYNOPSIS</span></span>
<span data-ttu-id="33417-103">Restaurar um espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="33417-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="33417-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33417-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33417-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33417-105">DESCRIPTION</span></span>
<span data-ttu-id="33417-106">Restaurar um espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="33417-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="33417-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33417-107">EXAMPLES</span></span>

### <span data-ttu-id="33417-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33417-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="33417-109">Restaurar espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="33417-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="33417-110">OS</span><span class="sxs-lookup"><span data-stu-id="33417-110">PARAMETERS</span></span>

### <span data-ttu-id="33417-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33417-111">-DefaultProfile</span></span>
<span data-ttu-id="33417-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33417-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33417-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33417-113">-Force</span></span>
<span data-ttu-id="33417-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="33417-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="33417-115">-Local</span><span class="sxs-lookup"><span data-stu-id="33417-115">-Location</span></span>
<span data-ttu-id="33417-116">A região geográfica na qual o espaço de trabalho será criado.</span><span class="sxs-lookup"><span data-stu-id="33417-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33417-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="33417-117">-Name</span></span>
<span data-ttu-id="33417-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="33417-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33417-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33417-119">-ResourceGroupName</span></span>
<span data-ttu-id="33417-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33417-120">The resource group name.</span></span>

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

### <span data-ttu-id="33417-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33417-121">-Confirm</span></span>
<span data-ttu-id="33417-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33417-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33417-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33417-123">-WhatIf</span></span>
<span data-ttu-id="33417-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33417-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33417-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33417-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33417-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33417-126">CommonParameters</span></span>
<span data-ttu-id="33417-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33417-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33417-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33417-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33417-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33417-129">INPUTS</span></span>

### <span data-ttu-id="33417-130">System. String</span><span class="sxs-lookup"><span data-stu-id="33417-130">System.String</span></span>

## <span data-ttu-id="33417-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33417-131">OUTPUTS</span></span>

### <span data-ttu-id="33417-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="33417-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="33417-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33417-133">NOTES</span></span>

## <span data-ttu-id="33417-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33417-134">RELATED LINKS</span></span>
