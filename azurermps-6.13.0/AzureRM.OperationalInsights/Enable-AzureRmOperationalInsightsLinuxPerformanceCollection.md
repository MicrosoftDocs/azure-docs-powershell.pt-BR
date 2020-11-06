---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 4bb969e0d18aca0f05663003c0fe78edf5b0e99d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428442"
---
# <span data-ttu-id="d7796-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="d7796-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="d7796-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7796-102">SYNOPSIS</span></span>
<span data-ttu-id="d7796-103">Inicia a coleta de contadores de desempenho a partir de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d7796-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7796-104">SYNTAX</span></span>

### <span data-ttu-id="d7796-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7796-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7796-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7796-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7796-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7796-107">DESCRIPTION</span></span>
<span data-ttu-id="d7796-108">O cmdlet **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** inicia a coleta de contadores de desempenho de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7796-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d7796-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7796-109">EXAMPLES</span></span>

## <span data-ttu-id="d7796-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7796-110">PARAMETERS</span></span>

### <span data-ttu-id="d7796-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7796-111">-DefaultProfile</span></span>
<span data-ttu-id="d7796-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d7796-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7796-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7796-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7796-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d7796-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d7796-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d7796-115">-Workspace</span></span>
<span data-ttu-id="d7796-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="d7796-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d7796-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d7796-117">-WorkspaceName</span></span>
<span data-ttu-id="d7796-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="d7796-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d7796-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7796-119">-Confirm</span></span>
<span data-ttu-id="d7796-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7796-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7796-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7796-121">-WhatIf</span></span>
<span data-ttu-id="d7796-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7796-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7796-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7796-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7796-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7796-124">CommonParameters</span></span>
<span data-ttu-id="d7796-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7796-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7796-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7796-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7796-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7796-127">INPUTS</span></span>

### <span data-ttu-id="d7796-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7796-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d7796-129">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7796-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d7796-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d7796-130">System.String</span></span>

## <span data-ttu-id="d7796-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7796-131">OUTPUTS</span></span>

### <span data-ttu-id="d7796-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d7796-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d7796-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7796-133">NOTES</span></span>
* <span data-ttu-id="d7796-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="d7796-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d7796-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7796-135">RELATED LINKS</span></span>

[<span data-ttu-id="d7796-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="d7796-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

