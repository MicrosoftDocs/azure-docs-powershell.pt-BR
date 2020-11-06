---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 44f5ffd63f2bb89f2e26d8ded6a0c7f64181bf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610915"
---
# <span data-ttu-id="a1112-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a1112-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="a1112-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1112-102">SYNOPSIS</span></span>
<span data-ttu-id="a1112-103">Interrompe a coleta de logs do IIS a partir de computadores.</span><span class="sxs-lookup"><span data-stu-id="a1112-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1112-104">SYNTAX</span></span>

### <span data-ttu-id="a1112-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1112-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1112-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a1112-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1112-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1112-107">DESCRIPTION</span></span>
<span data-ttu-id="a1112-108">O cmdlet **Disable-AzureRmOperationalInsightsIISLogCollection** interrompe a coleta de logs dos serviços de informações da Internet (IIS) em computadores conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1112-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="a1112-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1112-109">EXAMPLES</span></span>

## <span data-ttu-id="a1112-110">OS</span><span class="sxs-lookup"><span data-stu-id="a1112-110">PARAMETERS</span></span>

### <span data-ttu-id="a1112-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1112-111">-DefaultProfile</span></span>
<span data-ttu-id="a1112-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1112-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1112-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1112-113">-ResourceGroupName</span></span>
<span data-ttu-id="a1112-114">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="a1112-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a1112-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a1112-115">-Workspace</span></span>
<span data-ttu-id="a1112-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="a1112-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a1112-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1112-117">-WorkspaceName</span></span>
<span data-ttu-id="a1112-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="a1112-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a1112-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1112-119">-Confirm</span></span>
<span data-ttu-id="a1112-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1112-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1112-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1112-121">-WhatIf</span></span>
<span data-ttu-id="a1112-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1112-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1112-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1112-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1112-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1112-124">CommonParameters</span></span>
<span data-ttu-id="a1112-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1112-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1112-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1112-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1112-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1112-127">INPUTS</span></span>

### <span data-ttu-id="a1112-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1112-128">PSWorkspace</span></span>
<span data-ttu-id="a1112-129">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a1112-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a1112-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1112-130">OUTPUTS</span></span>

### <span data-ttu-id="a1112-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a1112-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a1112-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1112-132">NOTES</span></span>
* <span data-ttu-id="a1112-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="a1112-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a1112-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1112-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1112-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a1112-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


