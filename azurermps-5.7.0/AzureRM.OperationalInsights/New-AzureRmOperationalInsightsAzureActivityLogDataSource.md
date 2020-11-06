---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6b3009a37a314b70d258f597823f8da062970450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428137"
---
# <span data-ttu-id="1aba7-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="1aba7-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="1aba7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aba7-102">SYNOPSIS</span></span>
<span data-ttu-id="1aba7-103">Coletar log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="1aba7-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aba7-104">SYNTAX</span></span>

### <span data-ttu-id="1aba7-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1aba7-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aba7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1aba7-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aba7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1aba7-107">DESCRIPTION</span></span>
<span data-ttu-id="1aba7-108">O New-AzureRmOperationalInsightsAzureActivityLogDataSource habilitar a análise de logs para coletar o log de atividades do Azure de determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="1aba7-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="1aba7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aba7-109">EXAMPLES</span></span>

### <span data-ttu-id="1aba7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1aba7-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1aba7-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="1aba7-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1aba7-112">OS</span><span class="sxs-lookup"><span data-stu-id="1aba7-112">PARAMETERS</span></span>

### <span data-ttu-id="1aba7-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="1aba7-113">-BackfillStartTime</span></span>
<span data-ttu-id="1aba7-114">Você pode optar por fazer o aterramento de logs de uma semana atrás.</span><span class="sxs-lookup"><span data-stu-id="1aba7-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aba7-115">-DefaultProfile</span></span>
<span data-ttu-id="1aba7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1aba7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1aba7-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aba7-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aba7-119">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1aba7-120">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-121">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1aba7-121">-Workspace</span></span>
```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1aba7-122">-WorkspaceName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aba7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1aba7-123">-Confirm</span></span>
<span data-ttu-id="1aba7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aba7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aba7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aba7-125">-WhatIf</span></span>
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

### <span data-ttu-id="1aba7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aba7-126">CommonParameters</span></span>
<span data-ttu-id="1aba7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aba7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aba7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aba7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aba7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1aba7-129">INPUTS</span></span>

### <span data-ttu-id="1aba7-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1aba7-130">PSWorkspace</span></span>
<span data-ttu-id="1aba7-131">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1aba7-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1aba7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1aba7-132">OUTPUTS</span></span>

### <span data-ttu-id="1aba7-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1aba7-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1aba7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1aba7-134">NOTES</span></span>

## <span data-ttu-id="1aba7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aba7-135">RELATED LINKS</span></span>

