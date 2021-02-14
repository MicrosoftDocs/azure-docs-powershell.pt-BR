---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117295"
---
# <span data-ttu-id="78434-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="78434-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="78434-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78434-102">SYNOPSIS</span></span>
<span data-ttu-id="78434-103">Restaurar um espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="78434-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="78434-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78434-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78434-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="78434-105">DESCRIPTION</span></span>
<span data-ttu-id="78434-106">Restaurar um espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="78434-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="78434-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78434-107">EXAMPLES</span></span>

### <span data-ttu-id="78434-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78434-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="78434-109">Restaurar espaço de trabalho excluído.</span><span class="sxs-lookup"><span data-stu-id="78434-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="78434-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78434-110">PARAMETERS</span></span>

### <span data-ttu-id="78434-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78434-111">-DefaultProfile</span></span>
<span data-ttu-id="78434-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78434-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78434-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="78434-113">-Force</span></span>
<span data-ttu-id="78434-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="78434-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="78434-115">-Local</span><span class="sxs-lookup"><span data-stu-id="78434-115">-Location</span></span>
<span data-ttu-id="78434-116">A região geográfica em que o espaço de trabalho será criado.</span><span class="sxs-lookup"><span data-stu-id="78434-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="78434-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="78434-117">-Name</span></span>
<span data-ttu-id="78434-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="78434-118">The workspace name.</span></span>

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

### <span data-ttu-id="78434-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78434-119">-ResourceGroupName</span></span>
<span data-ttu-id="78434-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78434-120">The resource group name.</span></span>

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

### <span data-ttu-id="78434-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78434-121">-Confirm</span></span>
<span data-ttu-id="78434-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78434-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78434-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78434-123">-WhatIf</span></span>
<span data-ttu-id="78434-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78434-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78434-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78434-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78434-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78434-126">CommonParameters</span></span>
<span data-ttu-id="78434-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78434-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78434-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78434-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78434-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="78434-129">INPUTS</span></span>

### <span data-ttu-id="78434-130">System.String</span><span class="sxs-lookup"><span data-stu-id="78434-130">System.String</span></span>

## <span data-ttu-id="78434-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="78434-131">OUTPUTS</span></span>

### <span data-ttu-id="78434-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="78434-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="78434-133">Notas</span><span class="sxs-lookup"><span data-stu-id="78434-133">NOTES</span></span>

## <span data-ttu-id="78434-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78434-134">RELATED LINKS</span></span>
