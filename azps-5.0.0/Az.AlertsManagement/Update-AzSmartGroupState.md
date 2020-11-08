---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125078"
---
# <span data-ttu-id="0791c-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="0791c-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="0791c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0791c-102">SYNOPSIS</span></span>
<span data-ttu-id="0791c-103">Atualiza o estado do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="0791c-103">Updates smart group state</span></span>

## <span data-ttu-id="0791c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0791c-104">SYNTAX</span></span>

### <span data-ttu-id="0791c-105">BySmartGroupId (padrão)</span><span class="sxs-lookup"><span data-stu-id="0791c-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0791c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0791c-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0791c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0791c-107">DESCRIPTION</span></span>
<span data-ttu-id="0791c-108">**Update-AzSmartGroupState** cmdlet atualiza o estado do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="0791c-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="0791c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0791c-109">EXAMPLES</span></span>

### <span data-ttu-id="0791c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0791c-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="0791c-111">Esse cmdlet atualiza o estado do grupo inteligente para acknowleged.</span><span class="sxs-lookup"><span data-stu-id="0791c-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="0791c-112">OS</span><span class="sxs-lookup"><span data-stu-id="0791c-112">PARAMETERS</span></span>

### <span data-ttu-id="0791c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0791c-113">-DefaultProfile</span></span>
<span data-ttu-id="0791c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0791c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0791c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0791c-115">-InputObject</span></span>
<span data-ttu-id="0791c-116">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="0791c-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="0791c-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0791c-117">-SmartGroupId</span></span>
<span data-ttu-id="0791c-118">Identificador exclusivo do grupo inteligente/ResourceId do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="0791c-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="0791c-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="0791c-119">-State</span></span>
<span data-ttu-id="0791c-120">Estado do grupo inteligente atualizado</span><span class="sxs-lookup"><span data-stu-id="0791c-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="0791c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0791c-121">-Confirm</span></span>
<span data-ttu-id="0791c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0791c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0791c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0791c-123">-WhatIf</span></span>
<span data-ttu-id="0791c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0791c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0791c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0791c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0791c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0791c-126">CommonParameters</span></span>
<span data-ttu-id="0791c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0791c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0791c-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0791c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0791c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0791c-129">INPUTS</span></span>

### <span data-ttu-id="0791c-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0791c-130">None</span></span>

## <span data-ttu-id="0791c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0791c-131">OUTPUTS</span></span>

### <span data-ttu-id="0791c-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="0791c-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="0791c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0791c-133">NOTES</span></span>

## <span data-ttu-id="0791c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0791c-134">RELATED LINKS</span></span>
