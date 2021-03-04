---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 1ab5abc4af394647fd1438ed79cebb739daaca94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889590"
---
# <span data-ttu-id="92aca-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="92aca-101">Update-AzAlertState</span></span>

## <span data-ttu-id="92aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92aca-102">SYNOPSIS</span></span>
<span data-ttu-id="92aca-103">Estado de alerta de atualizações</span><span class="sxs-lookup"><span data-stu-id="92aca-103">Updates alert state</span></span>

## <span data-ttu-id="92aca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92aca-104">SYNTAX</span></span>

### <span data-ttu-id="92aca-105">ByAlertId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92aca-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92aca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92aca-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92aca-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92aca-107">DESCRIPTION</span></span>
<span data-ttu-id="92aca-108">O cmdlet **Update-AzAlertState** atualiza o estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="92aca-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="92aca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92aca-109">EXAMPLES</span></span>

### <span data-ttu-id="92aca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92aca-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="92aca-111">Este cmdlet atualiza o estado de alerta para Closed.</span><span class="sxs-lookup"><span data-stu-id="92aca-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="92aca-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92aca-112">PARAMETERS</span></span>

### <span data-ttu-id="92aca-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="92aca-113">-AlertId</span></span>
<span data-ttu-id="92aca-114">Identificador exclusivo de Alerta/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="92aca-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92aca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92aca-115">-DefaultProfile</span></span>
<span data-ttu-id="92aca-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92aca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92aca-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92aca-117">-InputObject</span></span>
<span data-ttu-id="92aca-118">Objeto input do pipeline.</span><span class="sxs-lookup"><span data-stu-id="92aca-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92aca-119">-State</span><span class="sxs-lookup"><span data-stu-id="92aca-119">-State</span></span>
<span data-ttu-id="92aca-120">Estado de alerta atualizado</span><span class="sxs-lookup"><span data-stu-id="92aca-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92aca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92aca-121">-Confirm</span></span>
<span data-ttu-id="92aca-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92aca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92aca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92aca-123">-WhatIf</span></span>
<span data-ttu-id="92aca-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92aca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92aca-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92aca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92aca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92aca-126">CommonParameters</span></span>
<span data-ttu-id="92aca-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92aca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92aca-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92aca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92aca-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92aca-129">INPUTS</span></span>

### <span data-ttu-id="92aca-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="92aca-130">None</span></span>

## <span data-ttu-id="92aca-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92aca-131">OUTPUTS</span></span>

### <span data-ttu-id="92aca-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="92aca-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="92aca-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="92aca-133">NOTES</span></span>

## <span data-ttu-id="92aca-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92aca-134">RELATED LINKS</span></span>
