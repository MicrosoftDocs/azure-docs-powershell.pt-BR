---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112948"
---
# <span data-ttu-id="20baa-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="20baa-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="20baa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20baa-102">SYNOPSIS</span></span>
<span data-ttu-id="20baa-103">Cria um objeto do tipo Grupo de Ações Azns</span><span class="sxs-lookup"><span data-stu-id="20baa-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="20baa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20baa-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20baa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20baa-105">DESCRIPTION</span></span>
<span data-ttu-id="20baa-106">Cria um objeto do tipo Grupo de Ações Azns.</span><span class="sxs-lookup"><span data-stu-id="20baa-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="20baa-107">Esse objeto deve ser passado para o comando que cria a Regra de Alerta de Log.</span><span class="sxs-lookup"><span data-stu-id="20baa-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="20baa-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20baa-108">EXAMPLES</span></span>

### <span data-ttu-id="20baa-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20baa-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="20baa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20baa-110">PARAMETERS</span></span>

### <span data-ttu-id="20baa-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="20baa-111">-ActionGroup</span></span>
<span data-ttu-id="20baa-112">A lista de grupos de ações para enviar notificação</span><span class="sxs-lookup"><span data-stu-id="20baa-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="20baa-113">-CustomWebwebpayload</span><span class="sxs-lookup"><span data-stu-id="20baa-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="20baa-114">A carga personalizada da Webload</span><span class="sxs-lookup"><span data-stu-id="20baa-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="20baa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20baa-115">-DefaultProfile</span></span>
<span data-ttu-id="20baa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20baa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20baa-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="20baa-117">-EmailSubject</span></span>
<span data-ttu-id="20baa-118">O assunto do email da notificação de alerta</span><span class="sxs-lookup"><span data-stu-id="20baa-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="20baa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20baa-119">CommonParameters</span></span>
<span data-ttu-id="20baa-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20baa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20baa-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20baa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20baa-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="20baa-122">INPUTS</span></span>

### <span data-ttu-id="20baa-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20baa-123">None</span></span>

## <span data-ttu-id="20baa-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="20baa-124">OUTPUTS</span></span>

### <span data-ttu-id="20baa-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="20baa-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="20baa-126">Notas</span><span class="sxs-lookup"><span data-stu-id="20baa-126">NOTES</span></span>

## <span data-ttu-id="20baa-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20baa-127">RELATED LINKS</span></span>
