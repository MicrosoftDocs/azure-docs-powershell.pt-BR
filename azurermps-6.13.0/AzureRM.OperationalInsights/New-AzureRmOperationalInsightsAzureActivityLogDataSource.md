---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 654663e9fdc44270266aa2872b7deb939be93e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429407"
---
# <span data-ttu-id="5f617-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="5f617-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="5f617-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f617-102">SYNOPSIS</span></span>
<span data-ttu-id="5f617-103">Coletar log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f617-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f617-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f617-104">SYNTAX</span></span>

### <span data-ttu-id="5f617-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f617-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f617-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5f617-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f617-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f617-107">DESCRIPTION</span></span>
<span data-ttu-id="5f617-108">O New-AzureRmOperationalInsightsAzureActivityLogDataSource habilitar a análise de logs para coletar o log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f617-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="5f617-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f617-109">EXAMPLES</span></span>

### <span data-ttu-id="5f617-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f617-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5f617-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="5f617-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="5f617-112">OS</span><span class="sxs-lookup"><span data-stu-id="5f617-112">PARAMETERS</span></span>

### <span data-ttu-id="5f617-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="5f617-113">-BackfillStartTime</span></span>
<span data-ttu-id="5f617-114">Você pode optar por fazer o aterramento de logs de uma semana atrás.</span><span class="sxs-lookup"><span data-stu-id="5f617-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="5f617-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f617-115">-DefaultProfile</span></span>
<span data-ttu-id="5f617-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5f617-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f617-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5f617-117">-Force</span></span>
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

### <span data-ttu-id="5f617-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f617-118">-Name</span></span>
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

### <span data-ttu-id="5f617-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f617-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5f617-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f617-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="5f617-121">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5f617-121">-Workspace</span></span>
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

### <span data-ttu-id="5f617-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f617-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="5f617-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f617-123">-Confirm</span></span>
<span data-ttu-id="5f617-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f617-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f617-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f617-125">-WhatIf</span></span>
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

### <span data-ttu-id="5f617-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f617-126">CommonParameters</span></span>
<span data-ttu-id="5f617-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f617-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f617-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f617-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f617-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f617-129">INPUTS</span></span>

### <span data-ttu-id="5f617-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f617-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="5f617-131">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f617-131">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="5f617-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5f617-132">System.String</span></span>

### <span data-ttu-id="5f617-133">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f617-133">System.DateTimeOffset</span></span>

## <span data-ttu-id="5f617-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f617-134">OUTPUTS</span></span>

### <span data-ttu-id="5f617-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5f617-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5f617-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f617-136">NOTES</span></span>

## <span data-ttu-id="5f617-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f617-137">RELATED LINKS</span></span>
