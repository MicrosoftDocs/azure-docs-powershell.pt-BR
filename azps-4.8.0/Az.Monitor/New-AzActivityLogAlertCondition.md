---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948186"
---
# <span data-ttu-id="88b4e-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="88b4e-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="88b4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="88b4e-103">Cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="88b4e-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="88b4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88b4e-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88b4e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="88b4e-106">O cmdlet **New-AzActivityLogAlertCondition** cria novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="88b4e-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="88b4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="88b4e-108">Exemplo 1: criar um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="88b4e-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="88b4e-109">Esse comando cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="88b4e-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="88b4e-110">**Observação** : quando esse cmdlet é usado com Set-AzActivityLogAlert pelo menos um desses objetos, passados como parâmetros, deve ter seu campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="88b4e-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="88b4e-111">Caso contrário, o back-end responderá com um 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="88b4e-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="88b4e-112">OS</span><span class="sxs-lookup"><span data-stu-id="88b4e-112">PARAMETERS</span></span>

### <span data-ttu-id="88b4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b4e-113">-DefaultProfile</span></span>
<span data-ttu-id="88b4e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="88b4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88b4e-115">-Igual</span><span class="sxs-lookup"><span data-stu-id="88b4e-115">-Equal</span></span>
<span data-ttu-id="88b4e-116">Especifica a propriedade Equals para a condição de folha.</span><span class="sxs-lookup"><span data-stu-id="88b4e-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="88b4e-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="88b4e-117">-Field</span></span>
<span data-ttu-id="88b4e-118">Especifica o campo para a condição.</span><span class="sxs-lookup"><span data-stu-id="88b4e-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="88b4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b4e-119">CommonParameters</span></span>
<span data-ttu-id="88b4e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b4e-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b4e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b4e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88b4e-122">INPUTS</span></span>

### <span data-ttu-id="88b4e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="88b4e-123">System.String</span></span>

## <span data-ttu-id="88b4e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88b4e-124">OUTPUTS</span></span>

### <span data-ttu-id="88b4e-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="88b4e-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="88b4e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88b4e-126">NOTES</span></span>

## <span data-ttu-id="88b4e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88b4e-127">RELATED LINKS</span></span>

[<span data-ttu-id="88b4e-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88b4e-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="88b4e-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88b4e-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="88b4e-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88b4e-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="88b4e-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88b4e-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="88b4e-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88b4e-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="88b4e-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="88b4e-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
