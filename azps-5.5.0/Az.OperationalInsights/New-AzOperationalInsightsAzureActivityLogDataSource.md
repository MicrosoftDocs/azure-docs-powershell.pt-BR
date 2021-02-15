---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112743"
---
# <span data-ttu-id="b13de-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="b13de-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="b13de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b13de-102">SYNOPSIS</span></span>
<span data-ttu-id="b13de-103">Coletar log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="b13de-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="b13de-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b13de-104">SYNTAX</span></span>

### <span data-ttu-id="b13de-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b13de-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13de-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b13de-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13de-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b13de-107">DESCRIPTION</span></span>
<span data-ttu-id="b13de-108">A New-AzOperationalInsightsAzureActivityLogDataSource habilitar o Log Analytics para coletar o log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="b13de-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="b13de-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b13de-109">EXAMPLES</span></span>

### <span data-ttu-id="b13de-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b13de-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b13de-111">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="b13de-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="b13de-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b13de-112">PARAMETERS</span></span>

### <span data-ttu-id="b13de-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="b13de-113">-BackfillStartTime</span></span>
<span data-ttu-id="b13de-114">Você pode optar por fazer o backfill logs de uma semana atrás.</span><span class="sxs-lookup"><span data-stu-id="b13de-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13de-115">-DefaultProfile</span></span>
<span data-ttu-id="b13de-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b13de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b13de-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b13de-117">-Force</span></span>
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

### <span data-ttu-id="b13de-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b13de-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13de-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b13de-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-121">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="b13de-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-122">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="b13de-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b13de-123">-Confirm</span></span>
<span data-ttu-id="b13de-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13de-125">-WhatIf</span></span>
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

### <span data-ttu-id="b13de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13de-126">CommonParameters</span></span>
<span data-ttu-id="b13de-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13de-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13de-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13de-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b13de-129">INPUTS</span></span>

### <span data-ttu-id="b13de-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b13de-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b13de-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b13de-131">System.String</span></span>

### <span data-ttu-id="b13de-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b13de-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="b13de-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="b13de-133">OUTPUTS</span></span>

### <span data-ttu-id="b13de-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b13de-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b13de-135">Notas</span><span class="sxs-lookup"><span data-stu-id="b13de-135">NOTES</span></span>

## <span data-ttu-id="b13de-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b13de-136">RELATED LINKS</span></span>
