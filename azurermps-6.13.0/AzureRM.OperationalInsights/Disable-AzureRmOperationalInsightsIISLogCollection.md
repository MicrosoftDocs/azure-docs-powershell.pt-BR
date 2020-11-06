---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602240"
---
# <span data-ttu-id="0cd51-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0cd51-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="0cd51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cd51-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd51-103">Interrompe a coleta de logs do IIS a partir de computadores.</span><span class="sxs-lookup"><span data-stu-id="0cd51-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cd51-104">SYNTAX</span></span>

### <span data-ttu-id="0cd51-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0cd51-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cd51-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0cd51-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cd51-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cd51-107">DESCRIPTION</span></span>
<span data-ttu-id="0cd51-108">O cmdlet **Disable-AzureRmOperationalInsightsIISLogCollection** interrompe a coleta de logs dos serviços de informações da Internet (IIS) em computadores conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0cd51-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="0cd51-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cd51-109">EXAMPLES</span></span>

## <span data-ttu-id="0cd51-110">OS</span><span class="sxs-lookup"><span data-stu-id="0cd51-110">PARAMETERS</span></span>

### <span data-ttu-id="0cd51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd51-111">-DefaultProfile</span></span>
<span data-ttu-id="0cd51-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0cd51-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cd51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd51-113">-ResourceGroupName</span></span>
<span data-ttu-id="0cd51-114">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="0cd51-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="0cd51-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0cd51-115">-Workspace</span></span>
<span data-ttu-id="0cd51-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="0cd51-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0cd51-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0cd51-117">-WorkspaceName</span></span>
<span data-ttu-id="0cd51-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="0cd51-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0cd51-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cd51-119">-Confirm</span></span>
<span data-ttu-id="0cd51-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd51-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd51-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd51-121">-WhatIf</span></span>
<span data-ttu-id="0cd51-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cd51-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd51-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cd51-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd51-124">CommonParameters</span></span>
<span data-ttu-id="0cd51-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd51-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd51-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cd51-127">INPUTS</span></span>

### <span data-ttu-id="0cd51-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0cd51-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="0cd51-129">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0cd51-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="0cd51-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0cd51-130">System.String</span></span>

## <span data-ttu-id="0cd51-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cd51-131">OUTPUTS</span></span>

### <span data-ttu-id="0cd51-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd51-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0cd51-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cd51-133">NOTES</span></span>
* <span data-ttu-id="0cd51-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="0cd51-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0cd51-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cd51-135">RELATED LINKS</span></span>

[<span data-ttu-id="0cd51-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0cd51-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


