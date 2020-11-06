---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: bca70877b8821b06e6662f334120f126328f4451
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440420"
---
# <span data-ttu-id="b9cdf-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9cdf-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="b9cdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b9cdf-103">Remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9cdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9cdf-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9cdf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9cdf-105">DESCRIPTION</span></span>
<span data-ttu-id="b9cdf-106">O cmdlet **Remove-AzureRmAlertRule** remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="b9cdf-107">Você deve especificar o nome da regra de alerta e o grupo de recursos ao qual ele está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="b9cdf-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b9cdf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="b9cdf-110">Exemplo 1: remover uma regra de alerta</span><span class="sxs-lookup"><span data-stu-id="b9cdf-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b9cdf-111">Esse comando Remove a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8 no grupo de recursos Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="b9cdf-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9cdf-112">PARAMETERS</span></span>

### <span data-ttu-id="b9cdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9cdf-113">-DefaultProfile</span></span>
<span data-ttu-id="b9cdf-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b9cdf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9cdf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9cdf-115">-Name</span></span>
<span data-ttu-id="b9cdf-116">Especifica o nome da regra de alerta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="b9cdf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9cdf-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9cdf-118">Especifica o nome do grupo de recursos para a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="b9cdf-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9cdf-119">-Confirm</span></span>
<span data-ttu-id="b9cdf-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9cdf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9cdf-121">-WhatIf</span></span>
<span data-ttu-id="b9cdf-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9cdf-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9cdf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9cdf-124">CommonParameters</span></span>
<span data-ttu-id="b9cdf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9cdf-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9cdf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9cdf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9cdf-127">INPUTS</span></span>

### <span data-ttu-id="b9cdf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b9cdf-128">System.String</span></span>

## <span data-ttu-id="b9cdf-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9cdf-129">OUTPUTS</span></span>

### <span data-ttu-id="b9cdf-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b9cdf-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b9cdf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9cdf-131">NOTES</span></span>

## <span data-ttu-id="b9cdf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9cdf-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9cdf-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9cdf-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b9cdf-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9cdf-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b9cdf-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b9cdf-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b9cdf-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9cdf-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


