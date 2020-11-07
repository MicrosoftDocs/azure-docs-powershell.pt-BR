---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941113"
---
# <span data-ttu-id="6cb44-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6cb44-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="6cb44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cb44-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb44-103">Cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="6cb44-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="6cb44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cb44-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cb44-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb44-106">O cmdlet **New-AzAlertRuleWebhook** cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="6cb44-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="6cb44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cb44-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb44-108">Exemplo 1: criar uma regra de alerta webhook</span><span class="sxs-lookup"><span data-stu-id="6cb44-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="6cb44-109">Esse comando cria um webhook de regra de alerta especificando somente o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb44-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="6cb44-110">Exemplo 2: criar um webhook com uma propriedade</span><span class="sxs-lookup"><span data-stu-id="6cb44-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="6cb44-111">Esse comando cria um webhook de regra de alerta para Contoso.com que tem uma propriedade e, em seguida, armazena-o na variável $Actual.</span><span class="sxs-lookup"><span data-stu-id="6cb44-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="6cb44-112">OS</span><span class="sxs-lookup"><span data-stu-id="6cb44-112">PARAMETERS</span></span>

### <span data-ttu-id="6cb44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb44-113">-DefaultProfile</span></span>
<span data-ttu-id="6cb44-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6cb44-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb44-115">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="6cb44-115">-Property</span></span>
<span data-ttu-id="6cb44-116">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="6cb44-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="6cb44-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6cb44-117">-ServiceUri</span></span>
<span data-ttu-id="6cb44-118">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb44-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="6cb44-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb44-119">CommonParameters</span></span>
<span data-ttu-id="6cb44-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb44-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb44-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb44-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb44-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cb44-122">INPUTS</span></span>

### <span data-ttu-id="6cb44-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb44-123">System.String</span></span>

### <span data-ttu-id="6cb44-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6cb44-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cb44-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cb44-125">OUTPUTS</span></span>

### <span data-ttu-id="6cb44-126">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="6cb44-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="6cb44-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cb44-127">NOTES</span></span>

## <span data-ttu-id="6cb44-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cb44-128">RELATED LINKS</span></span>

[<span data-ttu-id="6cb44-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6cb44-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="6cb44-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6cb44-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="6cb44-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6cb44-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="6cb44-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6cb44-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="6cb44-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="6cb44-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


