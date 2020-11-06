---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430700"
---
# <span data-ttu-id="462e8-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="462e8-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="462e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="462e8-102">SYNOPSIS</span></span>
<span data-ttu-id="462e8-103">Coletar log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="462e8-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="462e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="462e8-104">SYNTAX</span></span>

### <span data-ttu-id="462e8-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="462e8-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462e8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="462e8-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="462e8-107">DESCRIPTION</span></span>
<span data-ttu-id="462e8-108">O New-AzureRmOperationalInsightsAzureActivityLogDataSource habilitar a análise de logs para coletar o log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="462e8-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="462e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="462e8-109">EXAMPLES</span></span>

### <span data-ttu-id="462e8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="462e8-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="462e8-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="462e8-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="462e8-112">OS</span><span class="sxs-lookup"><span data-stu-id="462e8-112">PARAMETERS</span></span>

### <span data-ttu-id="462e8-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="462e8-113">-BackfillStartTime</span></span>
<span data-ttu-id="462e8-114">Você pode optar por fazer o aterramento de logs de uma semana atrás.</span><span class="sxs-lookup"><span data-stu-id="462e8-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="462e8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="462e8-115">-Force</span></span>
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

### <span data-ttu-id="462e8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="462e8-116">-Name</span></span>
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

### <span data-ttu-id="462e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462e8-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="462e8-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="462e8-118">-SubscriptionId</span></span>
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

### <span data-ttu-id="462e8-119">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="462e8-119">-Workspace</span></span>
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

### <span data-ttu-id="462e8-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="462e8-120">-WorkspaceName</span></span>
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

### <span data-ttu-id="462e8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="462e8-121">-Confirm</span></span>
<span data-ttu-id="462e8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="462e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462e8-123">-WhatIf</span></span>
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

### <span data-ttu-id="462e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462e8-124">-DefaultProfile</span></span>
<span data-ttu-id="462e8-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="462e8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="462e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462e8-126">CommonParameters</span></span>
<span data-ttu-id="462e8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="462e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462e8-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462e8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="462e8-129">INPUTS</span></span>

### <span data-ttu-id="462e8-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="462e8-130">PSWorkspace</span></span>
<span data-ttu-id="462e8-131">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="462e8-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="462e8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="462e8-132">OUTPUTS</span></span>

### <span data-ttu-id="462e8-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="462e8-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="462e8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="462e8-134">NOTES</span></span>

## <span data-ttu-id="462e8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="462e8-135">RELATED LINKS</span></span>

