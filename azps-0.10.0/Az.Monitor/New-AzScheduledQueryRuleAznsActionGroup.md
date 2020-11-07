---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 485f244caa78bffda71d6129990c76daa8b173c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775703"
---
# <span data-ttu-id="29fd2-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="29fd2-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="29fd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="29fd2-103">Cria um objeto do tipo Azns grupo de ação</span><span class="sxs-lookup"><span data-stu-id="29fd2-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="29fd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29fd2-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29fd2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="29fd2-106">Cria um objeto do tipo Azns grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="29fd2-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="29fd2-107">Esse objeto deve ser passado para o comando que cria a regra de alerta de log.</span><span class="sxs-lookup"><span data-stu-id="29fd2-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="29fd2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29fd2-108">EXAMPLES</span></span>

### <span data-ttu-id="29fd2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29fd2-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="29fd2-110">OS</span><span class="sxs-lookup"><span data-stu-id="29fd2-110">PARAMETERS</span></span>

### <span data-ttu-id="29fd2-111">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="29fd2-111">-ActionGroup</span></span>
<span data-ttu-id="29fd2-112">A lista de grupos de ações para enviar notificações</span><span class="sxs-lookup"><span data-stu-id="29fd2-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="29fd2-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="29fd2-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="29fd2-114">A carga do webhook personalizada</span><span class="sxs-lookup"><span data-stu-id="29fd2-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="29fd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fd2-115">-DefaultProfile</span></span>
<span data-ttu-id="29fd2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29fd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fd2-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="29fd2-117">-EmailSubject</span></span>
<span data-ttu-id="29fd2-118">O assunto do email da notificação de alerta</span><span class="sxs-lookup"><span data-stu-id="29fd2-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="29fd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fd2-119">CommonParameters</span></span>
<span data-ttu-id="29fd2-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29fd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fd2-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29fd2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fd2-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29fd2-122">INPUTS</span></span>

### <span data-ttu-id="29fd2-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="29fd2-123">None</span></span>

## <span data-ttu-id="29fd2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29fd2-124">OUTPUTS</span></span>

### <span data-ttu-id="29fd2-125">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="29fd2-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="29fd2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29fd2-126">NOTES</span></span>

## <span data-ttu-id="29fd2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29fd2-127">RELATED LINKS</span></span>