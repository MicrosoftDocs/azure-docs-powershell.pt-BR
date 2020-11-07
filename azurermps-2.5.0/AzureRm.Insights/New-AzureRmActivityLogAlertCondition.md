---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
ms.openlocfilehash: a7ad8616bf2afc79d049384c1f20002ff6d6aa4a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785249"
---
# <span data-ttu-id="b6b95-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b6b95-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="b6b95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6b95-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b95-103">Cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="b6b95-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6b95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6b95-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6b95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6b95-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b95-106">O cmdlet **New-AzureRmActivityLogAlertCondition** cria novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="b6b95-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="b6b95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6b95-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b95-108">Exemplo 1: criar um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="b6b95-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="b6b95-109">Esse comando cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="b6b95-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="b6b95-110">**Observação** : quando esse cmdlet é usado com Set-AzureRmActivityLogAlert pelo menos um desses objetos, passados como parâmetros, deve ter seu campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="b6b95-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="b6b95-111">Caso contrário, o back-end responderá com um 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="b6b95-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="b6b95-112">OS</span><span class="sxs-lookup"><span data-stu-id="b6b95-112">PARAMETERS</span></span>

### <span data-ttu-id="b6b95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b95-113">-DefaultProfile</span></span>
<span data-ttu-id="b6b95-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b6b95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-115">-Igual</span><span class="sxs-lookup"><span data-stu-id="b6b95-115">-Equal</span></span>
<span data-ttu-id="b6b95-116">Especifica a propriedade Equals para a condição de folha.</span><span class="sxs-lookup"><span data-stu-id="b6b95-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="b6b95-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="b6b95-117">-Field</span></span>
<span data-ttu-id="b6b95-118">Especifica o campo para a condição.</span><span class="sxs-lookup"><span data-stu-id="b6b95-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="b6b95-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b95-119">CommonParameters</span></span>
<span data-ttu-id="b6b95-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b95-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b95-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b95-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b95-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6b95-122">INPUTS</span></span>

### <span data-ttu-id="b6b95-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b95-123">System.String</span></span>

## <span data-ttu-id="b6b95-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6b95-124">OUTPUTS</span></span>

### <span data-ttu-id="b6b95-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="b6b95-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="b6b95-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6b95-126">NOTES</span></span>

## <span data-ttu-id="b6b95-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6b95-127">RELATED LINKS</span></span>

[<span data-ttu-id="b6b95-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b6b95-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b6b95-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b6b95-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b6b95-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b6b95-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b6b95-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b6b95-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b6b95-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b6b95-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b6b95-133">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b6b95-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
