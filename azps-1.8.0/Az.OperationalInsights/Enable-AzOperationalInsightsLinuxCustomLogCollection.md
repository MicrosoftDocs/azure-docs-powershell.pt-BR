---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 67858083ed648e2965ea6fad2900ab63ef453901
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599865"
---
# <span data-ttu-id="d8381-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d8381-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="d8381-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8381-102">SYNOPSIS</span></span>
<span data-ttu-id="d8381-103">Inicia a coleta de logs personalizados de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d8381-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="d8381-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8381-104">SYNTAX</span></span>

### <span data-ttu-id="d8381-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8381-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8381-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8381-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8381-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8381-107">DESCRIPTION</span></span>
<span data-ttu-id="d8381-108">O cmdlet **Enable-AzOperationalInsightsLinuxCustomLogCollection** inicia a coleta de logs personalizados de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8381-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d8381-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8381-109">EXAMPLES</span></span>

## <span data-ttu-id="d8381-110">OS</span><span class="sxs-lookup"><span data-stu-id="d8381-110">PARAMETERS</span></span>

### <span data-ttu-id="d8381-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8381-111">-DefaultProfile</span></span>
<span data-ttu-id="d8381-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d8381-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8381-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8381-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8381-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d8381-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d8381-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d8381-115">-Workspace</span></span>
<span data-ttu-id="d8381-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="d8381-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d8381-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8381-117">-WorkspaceName</span></span>
<span data-ttu-id="d8381-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="d8381-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d8381-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8381-119">-Confirm</span></span>
<span data-ttu-id="d8381-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8381-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8381-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8381-121">-WhatIf</span></span>
<span data-ttu-id="d8381-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8381-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8381-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8381-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8381-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8381-124">CommonParameters</span></span>
<span data-ttu-id="d8381-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8381-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8381-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8381-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8381-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8381-127">INPUTS</span></span>

### <span data-ttu-id="d8381-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8381-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d8381-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d8381-129">System.String</span></span>

## <span data-ttu-id="d8381-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8381-130">OUTPUTS</span></span>

### <span data-ttu-id="d8381-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d8381-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d8381-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8381-132">NOTES</span></span>
* <span data-ttu-id="d8381-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="d8381-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d8381-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8381-134">RELATED LINKS</span></span>

[<span data-ttu-id="d8381-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d8381-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


