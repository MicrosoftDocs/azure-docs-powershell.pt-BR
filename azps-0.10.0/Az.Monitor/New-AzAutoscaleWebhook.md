---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: a719d841df2d3f211fdb2592ed2a96b507c51e10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775711"
---
# <span data-ttu-id="eb789-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="eb789-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="eb789-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb789-102">SYNOPSIS</span></span>
<span data-ttu-id="eb789-103">Cria um webhook de autoescala.</span><span class="sxs-lookup"><span data-stu-id="eb789-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="eb789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb789-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb789-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb789-105">DESCRIPTION</span></span>
<span data-ttu-id="eb789-106">O cmdlet **New-AzAutoscaleWebhook** cria um webhook de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="eb789-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="eb789-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb789-107">EXAMPLES</span></span>

## <span data-ttu-id="eb789-108">OS</span><span class="sxs-lookup"><span data-stu-id="eb789-108">PARAMETERS</span></span>

### <span data-ttu-id="eb789-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb789-109">-DefaultProfile</span></span>
<span data-ttu-id="eb789-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="eb789-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb789-111">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="eb789-111">-Property</span></span>
<span data-ttu-id="eb789-112">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="eb789-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="eb789-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="eb789-113">-ServiceUri</span></span>
<span data-ttu-id="eb789-114">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="eb789-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="eb789-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb789-115">CommonParameters</span></span>
<span data-ttu-id="eb789-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb789-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb789-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb789-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb789-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb789-118">INPUTS</span></span>

### <span data-ttu-id="eb789-119">System. String</span><span class="sxs-lookup"><span data-stu-id="eb789-119">System.String</span></span>

### <span data-ttu-id="eb789-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb789-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb789-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb789-121">OUTPUTS</span></span>

### <span data-ttu-id="eb789-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="eb789-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="eb789-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb789-123">NOTES</span></span>

## <span data-ttu-id="eb789-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb789-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb789-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="eb789-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


