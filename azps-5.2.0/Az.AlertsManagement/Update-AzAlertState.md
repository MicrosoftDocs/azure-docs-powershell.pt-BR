---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257386"
---
# <span data-ttu-id="3dbab-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="3dbab-101">Update-AzAlertState</span></span>

## <span data-ttu-id="3dbab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dbab-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbab-103">Atualiza o estado do alerta</span><span class="sxs-lookup"><span data-stu-id="3dbab-103">Updates alert state</span></span>

## <span data-ttu-id="3dbab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dbab-104">SYNTAX</span></span>

### <span data-ttu-id="3dbab-105">ByAlertId (padrão)</span><span class="sxs-lookup"><span data-stu-id="3dbab-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dbab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3dbab-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dbab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3dbab-107">DESCRIPTION</span></span>
<span data-ttu-id="3dbab-108">**Update-AzAlertState** cmdlet atualiza o estado do alerta.</span><span class="sxs-lookup"><span data-stu-id="3dbab-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="3dbab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dbab-109">EXAMPLES</span></span>

### <span data-ttu-id="3dbab-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3dbab-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="3dbab-111">Este cmdlet atualiza o estado do alerta para Closed.</span><span class="sxs-lookup"><span data-stu-id="3dbab-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="3dbab-112">OS</span><span class="sxs-lookup"><span data-stu-id="3dbab-112">PARAMETERS</span></span>

### <span data-ttu-id="3dbab-113">-Alertid</span><span class="sxs-lookup"><span data-stu-id="3dbab-113">-AlertId</span></span>
<span data-ttu-id="3dbab-114">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="3dbab-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="3dbab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbab-115">-DefaultProfile</span></span>
<span data-ttu-id="3dbab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dbab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dbab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dbab-117">-InputObject</span></span>
<span data-ttu-id="3dbab-118">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3dbab-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="3dbab-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="3dbab-119">-State</span></span>
<span data-ttu-id="3dbab-120">Estado de alerta atualizado</span><span class="sxs-lookup"><span data-stu-id="3dbab-120">Updated Alert State</span></span>

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

### <span data-ttu-id="3dbab-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3dbab-121">-Confirm</span></span>
<span data-ttu-id="3dbab-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dbab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dbab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dbab-123">-WhatIf</span></span>
<span data-ttu-id="3dbab-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3dbab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dbab-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3dbab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dbab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbab-126">CommonParameters</span></span>
<span data-ttu-id="3dbab-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dbab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbab-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dbab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbab-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3dbab-129">INPUTS</span></span>

### <span data-ttu-id="3dbab-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3dbab-130">None</span></span>

## <span data-ttu-id="3dbab-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3dbab-131">OUTPUTS</span></span>

### <span data-ttu-id="3dbab-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="3dbab-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="3dbab-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3dbab-133">NOTES</span></span>

## <span data-ttu-id="3dbab-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dbab-134">RELATED LINKS</span></span>
