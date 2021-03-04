---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 5f7e0f26461780b30dbe2b80c79bad8231590e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901523"
---
# <span data-ttu-id="df9db-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="df9db-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="df9db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df9db-102">SYNOPSIS</span></span>
<span data-ttu-id="df9db-103">Atualiza o estado do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="df9db-103">Updates smart group state</span></span>

## <span data-ttu-id="df9db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df9db-104">SYNTAX</span></span>

### <span data-ttu-id="df9db-105">BySmartGroupId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df9db-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9db-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df9db-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9db-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df9db-107">DESCRIPTION</span></span>
<span data-ttu-id="df9db-108">O cmdlet **Update-AzSmartGroupState** atualiza o estado do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="df9db-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="df9db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df9db-109">EXAMPLES</span></span>

### <span data-ttu-id="df9db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df9db-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="df9db-111">Este cmdlet atualiza o estado do grupo inteligente para Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="df9db-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="df9db-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df9db-112">PARAMETERS</span></span>

### <span data-ttu-id="df9db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9db-113">-DefaultProfile</span></span>
<span data-ttu-id="df9db-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df9db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9db-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df9db-115">-InputObject</span></span>
<span data-ttu-id="df9db-116">Objeto input do pipeline.</span><span class="sxs-lookup"><span data-stu-id="df9db-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df9db-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="df9db-117">-SmartGroupId</span></span>
<span data-ttu-id="df9db-118">Identificador exclusivo do Grupo Inteligente/ResourceId do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="df9db-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9db-119">-State</span><span class="sxs-lookup"><span data-stu-id="df9db-119">-State</span></span>
<span data-ttu-id="df9db-120">Estado do grupo Smart atualizado</span><span class="sxs-lookup"><span data-stu-id="df9db-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="df9db-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df9db-121">-Confirm</span></span>
<span data-ttu-id="df9db-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9db-123">-WhatIf</span></span>
<span data-ttu-id="df9db-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df9db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9db-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df9db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9db-126">CommonParameters</span></span>
<span data-ttu-id="df9db-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9db-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df9db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9db-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df9db-129">INPUTS</span></span>

### <span data-ttu-id="df9db-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df9db-130">None</span></span>

## <span data-ttu-id="df9db-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df9db-131">OUTPUTS</span></span>

### <span data-ttu-id="df9db-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="df9db-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="df9db-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="df9db-133">NOTES</span></span>

## <span data-ttu-id="df9db-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df9db-134">RELATED LINKS</span></span>
