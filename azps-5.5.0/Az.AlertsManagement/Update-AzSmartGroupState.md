---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116661"
---
# <span data-ttu-id="75254-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="75254-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="75254-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75254-102">SYNOPSIS</span></span>
<span data-ttu-id="75254-103">Atualiza o estado do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="75254-103">Updates smart group state</span></span>

## <span data-ttu-id="75254-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75254-104">SYNTAX</span></span>

### <span data-ttu-id="75254-105">BySmartGroupId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75254-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75254-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="75254-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75254-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="75254-107">DESCRIPTION</span></span>
<span data-ttu-id="75254-108">**O cmdlet Update-AzSmartGroupState** atualiza o estado do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="75254-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="75254-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75254-109">EXAMPLES</span></span>

### <span data-ttu-id="75254-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75254-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="75254-111">Este cmdlet atualiza o estado do grupo inteligente para Acleged.</span><span class="sxs-lookup"><span data-stu-id="75254-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="75254-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75254-112">PARAMETERS</span></span>

### <span data-ttu-id="75254-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75254-113">-DefaultProfile</span></span>
<span data-ttu-id="75254-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75254-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75254-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75254-115">-InputObject</span></span>
<span data-ttu-id="75254-116">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="75254-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="75254-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="75254-117">-SmartGroupId</span></span>
<span data-ttu-id="75254-118">Identificador Exclusivo do Grupo Inteligente/ResourceId do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="75254-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="75254-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="75254-119">-State</span></span>
<span data-ttu-id="75254-120">Estado do grupo Smart atualizado</span><span class="sxs-lookup"><span data-stu-id="75254-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="75254-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="75254-121">-Confirm</span></span>
<span data-ttu-id="75254-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75254-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75254-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75254-123">-WhatIf</span></span>
<span data-ttu-id="75254-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="75254-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75254-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75254-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75254-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75254-126">CommonParameters</span></span>
<span data-ttu-id="75254-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75254-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75254-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75254-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75254-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="75254-129">INPUTS</span></span>

### <span data-ttu-id="75254-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75254-130">None</span></span>

## <span data-ttu-id="75254-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="75254-131">OUTPUTS</span></span>

### <span data-ttu-id="75254-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="75254-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="75254-133">Notas</span><span class="sxs-lookup"><span data-stu-id="75254-133">NOTES</span></span>

## <span data-ttu-id="75254-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75254-134">RELATED LINKS</span></span>
