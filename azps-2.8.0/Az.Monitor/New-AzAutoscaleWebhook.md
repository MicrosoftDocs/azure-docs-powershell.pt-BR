---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: 4f2e7ea3293c9ca40271b9092673f33108a9f1be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771863"
---
# <span data-ttu-id="26f40-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="26f40-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="26f40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26f40-102">SYNOPSIS</span></span>
<span data-ttu-id="26f40-103">Cria um webhook de autoescala.</span><span class="sxs-lookup"><span data-stu-id="26f40-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="26f40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26f40-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26f40-105">DESCRIPTION</span></span>
<span data-ttu-id="26f40-106">O cmdlet **New-AzAutoscaleWebhook** cria um webhook de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="26f40-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="26f40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26f40-107">EXAMPLES</span></span>

## <span data-ttu-id="26f40-108">OS</span><span class="sxs-lookup"><span data-stu-id="26f40-108">PARAMETERS</span></span>

### <span data-ttu-id="26f40-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f40-109">-DefaultProfile</span></span>
<span data-ttu-id="26f40-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="26f40-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26f40-111">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="26f40-111">-Property</span></span>
<span data-ttu-id="26f40-112">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="26f40-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="26f40-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="26f40-113">-ServiceUri</span></span>
<span data-ttu-id="26f40-114">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="26f40-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="26f40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f40-115">CommonParameters</span></span>
<span data-ttu-id="26f40-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f40-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26f40-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f40-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26f40-118">INPUTS</span></span>

### <span data-ttu-id="26f40-119">System. String</span><span class="sxs-lookup"><span data-stu-id="26f40-119">System.String</span></span>

### <span data-ttu-id="26f40-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26f40-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26f40-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26f40-121">OUTPUTS</span></span>

### <span data-ttu-id="26f40-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="26f40-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="26f40-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26f40-123">NOTES</span></span>

## <span data-ttu-id="26f40-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26f40-124">RELATED LINKS</span></span>

[<span data-ttu-id="26f40-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="26f40-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


