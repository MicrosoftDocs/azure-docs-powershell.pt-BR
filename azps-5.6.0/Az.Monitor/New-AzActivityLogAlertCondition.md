---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: f18479f8cf42c68a7c8a8a5d9f45a4542a758212
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888873"
---
# <span data-ttu-id="fe8d6-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="fe8d6-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="fe8d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8d6-103">Cria um novo objeto de condição de alerta de log de atividade na memória.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="fe8d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe8d6-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe8d6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe8d6-106">O cmdlet **New-AzActivityLogAlertCondition** cria um novo objeto de condição de alerta de log de atividade na memória.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="fe8d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe8d6-108">Exemplo 1: Criar um novo objeto de condição de alerta de log de atividade na memória.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="fe8d6-109">Este comando cria um novo objeto de condição de alerta de log de atividade na memória.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="fe8d6-110">**OBSERVAÇÃO**: quando esse cmdlet é usado com [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) pelo menos um desses objetos, passados como parâmetros, deve ter seu Field igual a "Category".</span><span class="sxs-lookup"><span data-stu-id="fe8d6-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="fe8d6-111">Caso contrário, o back-end responde com um 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="fe8d6-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="fe8d6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-112">PARAMETERS</span></span>

### <span data-ttu-id="fe8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="fe8d6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fe8d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe8d6-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="fe8d6-115">-Equal</span></span>
<span data-ttu-id="fe8d6-116">Especifica a propriedade equals para a condição de folha.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="fe8d6-117">-Field</span><span class="sxs-lookup"><span data-stu-id="fe8d6-117">-Field</span></span>
<span data-ttu-id="fe8d6-118">Especifica o campo da condição.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="fe8d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8d6-119">CommonParameters</span></span>
<span data-ttu-id="fe8d6-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe8d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8d6-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe8d6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8d6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-122">INPUTS</span></span>

### <span data-ttu-id="fe8d6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fe8d6-123">System.String</span></span>

## <span data-ttu-id="fe8d6-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-124">OUTPUTS</span></span>

### <span data-ttu-id="fe8d6-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="fe8d6-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="fe8d6-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe8d6-126">NOTES</span></span>

## <span data-ttu-id="fe8d6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe8d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="fe8d6-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe8d6-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="fe8d6-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe8d6-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="fe8d6-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe8d6-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="fe8d6-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe8d6-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="fe8d6-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe8d6-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="fe8d6-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="fe8d6-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
