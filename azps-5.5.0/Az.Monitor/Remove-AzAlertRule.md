---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118416"
---
# <span data-ttu-id="fd9da-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd9da-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="fd9da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd9da-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9da-103">Remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="fd9da-103">Removes an alert rule.</span></span>

## <span data-ttu-id="fd9da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd9da-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd9da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd9da-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9da-106">O **cmdlet Remove-AzAlertRule** remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="fd9da-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="fd9da-107">Você deve especificar o nome da regra de alerta e o grupo de recursos ao qual ela está atribuída.</span><span class="sxs-lookup"><span data-stu-id="fd9da-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="fd9da-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="fd9da-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="fd9da-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd9da-109">EXAMPLES</span></span>

### <span data-ttu-id="fd9da-110">Exemplo 1: Remover uma regra de alerta</span><span class="sxs-lookup"><span data-stu-id="fd9da-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="fd9da-111">Esse comando remove a regra de alerta chamada myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 no grupo de recursos Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="fd9da-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="fd9da-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd9da-112">PARAMETERS</span></span>

### <span data-ttu-id="fd9da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9da-113">-DefaultProfile</span></span>
<span data-ttu-id="fd9da-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fd9da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd9da-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd9da-115">-Name</span></span>
<span data-ttu-id="fd9da-116">Especifica o nome da regra de alerta a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fd9da-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9da-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd9da-118">Especifica o nome do grupo de recursos para a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="fd9da-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9da-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd9da-119">-Confirm</span></span>
<span data-ttu-id="fd9da-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9da-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd9da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9da-121">-WhatIf</span></span>
<span data-ttu-id="fd9da-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd9da-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd9da-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd9da-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd9da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9da-124">CommonParameters</span></span>
<span data-ttu-id="fd9da-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9da-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd9da-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9da-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd9da-127">INPUTS</span></span>

### <span data-ttu-id="fd9da-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fd9da-128">System.String</span></span>

## <span data-ttu-id="fd9da-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd9da-129">OUTPUTS</span></span>

### <span data-ttu-id="fd9da-130">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fd9da-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="fd9da-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fd9da-131">NOTES</span></span>

## <span data-ttu-id="fd9da-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd9da-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd9da-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd9da-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="fd9da-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd9da-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="fd9da-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="fd9da-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="fd9da-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd9da-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


