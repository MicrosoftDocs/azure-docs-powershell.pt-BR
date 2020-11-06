---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 0a7bbc6832c5a0c6c871d2a5c35ac9ee86042fd0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599849"
---
# <span data-ttu-id="2bd3f-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="2bd3f-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="2bd3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd3f-103">Coletar log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="2bd3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bd3f-104">SYNTAX</span></span>

### <span data-ttu-id="2bd3f-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2bd3f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd3f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2bd3f-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd3f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bd3f-107">DESCRIPTION</span></span>
<span data-ttu-id="2bd3f-108">O New-AzOperationalInsightsAzureActivityLogDataSource habilitar a análise de logs para coletar o log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="2bd3f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bd3f-109">EXAMPLES</span></span>

### <span data-ttu-id="2bd3f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bd3f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2bd3f-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="2bd3f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2bd3f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2bd3f-112">PARAMETERS</span></span>

### <span data-ttu-id="2bd3f-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="2bd3f-113">-BackfillStartTime</span></span>
<span data-ttu-id="2bd3f-114">Você pode optar por fazer o aterramento de logs de uma semana atrás.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="2bd3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd3f-115">-DefaultProfile</span></span>
<span data-ttu-id="2bd3f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2bd3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bd3f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2bd3f-117">-Force</span></span>
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

### <span data-ttu-id="2bd3f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bd3f-118">-Name</span></span>
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

### <span data-ttu-id="2bd3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd3f-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2bd3f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bd3f-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="2bd3f-121">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2bd3f-121">-Workspace</span></span>
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

### <span data-ttu-id="2bd3f-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2bd3f-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="2bd3f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bd3f-123">-Confirm</span></span>
<span data-ttu-id="2bd3f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd3f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd3f-125">-WhatIf</span></span>
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

### <span data-ttu-id="2bd3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd3f-126">CommonParameters</span></span>
<span data-ttu-id="2bd3f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd3f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd3f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd3f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bd3f-129">INPUTS</span></span>

### <span data-ttu-id="2bd3f-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bd3f-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2bd3f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd3f-131">System.String</span></span>

### <span data-ttu-id="2bd3f-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2bd3f-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="2bd3f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bd3f-133">OUTPUTS</span></span>

### <span data-ttu-id="2bd3f-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2bd3f-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2bd3f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bd3f-135">NOTES</span></span>

## <span data-ttu-id="2bd3f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bd3f-136">RELATED LINKS</span></span>
