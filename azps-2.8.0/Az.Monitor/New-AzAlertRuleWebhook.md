---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 1b8d58c6519084db5e679d3087c22adab7c2bef6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403996"
---
# <span data-ttu-id="49b4c-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="49b4c-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="49b4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="49b4c-103">Cria uma webfura de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="49b4c-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="49b4c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49b4c-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b4c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="49b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="49b4c-106">O **cmdlet New-AzAlertRuleWebweblet** cria uma weberte de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="49b4c-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="49b4c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="49b4c-108">Exemplo 1: Criar uma webtareia de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="49b4c-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="49b4c-109">Esse comando cria uma webião de regra de alerta especificando apenas o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="49b4c-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="49b4c-110">Exemplo 2: Criar uma webção com uma propriedade</span><span class="sxs-lookup"><span data-stu-id="49b4c-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="49b4c-111">Esse comando cria um web Contoso.com de regra de alerta que tem uma propriedade e a armazena na variável $Actual alerta.</span><span class="sxs-lookup"><span data-stu-id="49b4c-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="49b4c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="49b4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b4c-113">-DefaultProfile</span></span>
<span data-ttu-id="49b4c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="49b4c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49b4c-115">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="49b4c-115">-Property</span></span>
<span data-ttu-id="49b4c-116">Especifica a lista de propriedades no formato @(propriedade1 = 'valor1',....).</span><span class="sxs-lookup"><span data-stu-id="49b4c-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="49b4c-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="49b4c-117">-ServiceUri</span></span>
<span data-ttu-id="49b4c-118">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="49b4c-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="49b4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b4c-119">CommonParameters</span></span>
<span data-ttu-id="49b4c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b4c-121">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b4c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b4c-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="49b4c-122">INPUTS</span></span>

### <span data-ttu-id="49b4c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="49b4c-123">System.String</span></span>

### <span data-ttu-id="49b4c-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="49b4c-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49b4c-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="49b4c-125">OUTPUTS</span></span>

### <span data-ttu-id="49b4c-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebwebaction</span><span class="sxs-lookup"><span data-stu-id="49b4c-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="49b4c-127">Notas</span><span class="sxs-lookup"><span data-stu-id="49b4c-127">NOTES</span></span>

## <span data-ttu-id="49b4c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49b4c-128">RELATED LINKS</span></span>


[<span data-ttu-id="49b4c-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="49b4c-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="49b4c-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="49b4c-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="49b4c-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="49b4c-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="49b4c-132">New-AzAutoscaleWebwebscale</span><span class="sxs-lookup"><span data-stu-id="49b4c-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


