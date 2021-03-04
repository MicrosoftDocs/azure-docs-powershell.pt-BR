---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: b5bfac31babfd4bc848f9619dc8eb8cecd1c3eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893264"
---
# <span data-ttu-id="8c9e6-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8c9e6-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="8c9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9e6-103">Cria um objeto do tipo Grupo de Ações do Azns</span><span class="sxs-lookup"><span data-stu-id="8c9e6-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="8c9e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c9e6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9e6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9e6-106">Cria um objeto do tipo Grupo de Ações do Azns.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="8c9e6-107">Esse objeto deve ser passado para o comando que cria a Regra de Alerta de Log.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="8c9e6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-108">EXAMPLES</span></span>

### <span data-ttu-id="8c9e6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c9e6-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="8c9e6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-110">PARAMETERS</span></span>

### <span data-ttu-id="8c9e6-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="8c9e6-111">-ActionGroup</span></span>
<span data-ttu-id="8c9e6-112">A lista de grupos de ações a ser enviado para notificação</span><span class="sxs-lookup"><span data-stu-id="8c9e6-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9e6-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="8c9e6-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="8c9e6-114">A carga de webhook personalizada</span><span class="sxs-lookup"><span data-stu-id="8c9e6-114">The customized webhook payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9e6-115">-DefaultProfile</span></span>
<span data-ttu-id="8c9e6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c9e6-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="8c9e6-117">-EmailSubject</span></span>
<span data-ttu-id="8c9e6-118">O assunto do email de notificação de alerta</span><span class="sxs-lookup"><span data-stu-id="8c9e6-118">The email subject of alert notification</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9e6-119">CommonParameters</span></span>
<span data-ttu-id="8c9e6-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9e6-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c9e6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9e6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-122">INPUTS</span></span>

### <span data-ttu-id="8c9e6-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8c9e6-123">None</span></span>

## <span data-ttu-id="8c9e6-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-124">OUTPUTS</span></span>

### <span data-ttu-id="8c9e6-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="8c9e6-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="8c9e6-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c9e6-126">NOTES</span></span>

## <span data-ttu-id="8c9e6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c9e6-127">RELATED LINKS</span></span>
