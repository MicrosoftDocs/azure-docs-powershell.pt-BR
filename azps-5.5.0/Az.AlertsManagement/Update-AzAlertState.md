---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118105"
---
# <span data-ttu-id="2b727-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="2b727-101">Update-AzAlertState</span></span>

## <span data-ttu-id="2b727-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b727-102">SYNOPSIS</span></span>
<span data-ttu-id="2b727-103">Estado de alerta de atualizações</span><span class="sxs-lookup"><span data-stu-id="2b727-103">Updates alert state</span></span>

## <span data-ttu-id="2b727-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b727-104">SYNTAX</span></span>

### <span data-ttu-id="2b727-105">ByAlertId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b727-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b727-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b727-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b727-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b727-107">DESCRIPTION</span></span>
<span data-ttu-id="2b727-108">**O cmdlet Update-AzAlertState** atualiza o estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="2b727-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="2b727-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b727-109">EXAMPLES</span></span>

### <span data-ttu-id="2b727-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b727-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="2b727-111">Este cmdlet atualiza o estado de alerta para Fechado.</span><span class="sxs-lookup"><span data-stu-id="2b727-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="2b727-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b727-112">PARAMETERS</span></span>

### <span data-ttu-id="2b727-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="2b727-113">-AlertId</span></span>
<span data-ttu-id="2b727-114">Identificador exclusivo de alerta/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="2b727-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="2b727-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b727-115">-DefaultProfile</span></span>
<span data-ttu-id="2b727-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b727-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b727-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b727-117">-InputObject</span></span>
<span data-ttu-id="2b727-118">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b727-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="2b727-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="2b727-119">-State</span></span>
<span data-ttu-id="2b727-120">Estado de Alerta Atualizado</span><span class="sxs-lookup"><span data-stu-id="2b727-120">Updated Alert State</span></span>

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

### <span data-ttu-id="2b727-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2b727-121">-Confirm</span></span>
<span data-ttu-id="2b727-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b727-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b727-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b727-123">-WhatIf</span></span>
<span data-ttu-id="2b727-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2b727-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b727-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b727-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b727-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b727-126">CommonParameters</span></span>
<span data-ttu-id="2b727-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b727-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b727-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b727-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b727-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b727-129">INPUTS</span></span>

### <span data-ttu-id="2b727-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2b727-130">None</span></span>

## <span data-ttu-id="2b727-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b727-131">OUTPUTS</span></span>

### <span data-ttu-id="2b727-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="2b727-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="2b727-133">Notas</span><span class="sxs-lookup"><span data-stu-id="2b727-133">NOTES</span></span>

## <span data-ttu-id="2b727-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b727-134">RELATED LINKS</span></span>
