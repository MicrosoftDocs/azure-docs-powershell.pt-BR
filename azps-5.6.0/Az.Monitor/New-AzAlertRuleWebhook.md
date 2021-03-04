---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 22afc323e827c543150bffb317f1b5db5275d82c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888871"
---
# <span data-ttu-id="8516e-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="8516e-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="8516e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8516e-102">SYNOPSIS</span></span>
<span data-ttu-id="8516e-103">Cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="8516e-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="8516e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8516e-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8516e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8516e-105">DESCRIPTION</span></span>
<span data-ttu-id="8516e-106">O cmdlet **New-AzAlertRuleWebhook** cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="8516e-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="8516e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8516e-107">EXAMPLES</span></span>

### <span data-ttu-id="8516e-108">Exemplo 1: Criar um webhook de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="8516e-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="8516e-109">Este comando cria um webhook de regra de alerta especificando apenas o URI de serviço.</span><span class="sxs-lookup"><span data-stu-id="8516e-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="8516e-110">Exemplo 2: Criar um webhook com uma propriedade</span><span class="sxs-lookup"><span data-stu-id="8516e-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="8516e-111">Este comando cria um webhook de regra de alerta para Contoso.com que tem uma propriedade e, em seguida, o armazena na variável $Actual de segurança.</span><span class="sxs-lookup"><span data-stu-id="8516e-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="8516e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8516e-112">PARAMETERS</span></span>

### <span data-ttu-id="8516e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8516e-113">-DefaultProfile</span></span>
<span data-ttu-id="8516e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8516e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8516e-115">-Property</span><span class="sxs-lookup"><span data-stu-id="8516e-115">-Property</span></span>
<span data-ttu-id="8516e-116">Especifica a lista de propriedades no formato @(property1 = 'value1',....).</span><span class="sxs-lookup"><span data-stu-id="8516e-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8516e-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="8516e-117">-ServiceUri</span></span>
<span data-ttu-id="8516e-118">Especifica o URI de serviço.</span><span class="sxs-lookup"><span data-stu-id="8516e-118">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8516e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8516e-119">CommonParameters</span></span>
<span data-ttu-id="8516e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8516e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8516e-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8516e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8516e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8516e-122">INPUTS</span></span>

### <span data-ttu-id="8516e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8516e-123">System.String</span></span>

### <span data-ttu-id="8516e-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8516e-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8516e-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8516e-125">OUTPUTS</span></span>

### <span data-ttu-id="8516e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="8516e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="8516e-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="8516e-127">NOTES</span></span>

## <span data-ttu-id="8516e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8516e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8516e-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="8516e-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="8516e-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="8516e-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="8516e-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="8516e-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="8516e-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="8516e-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="8516e-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="8516e-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


