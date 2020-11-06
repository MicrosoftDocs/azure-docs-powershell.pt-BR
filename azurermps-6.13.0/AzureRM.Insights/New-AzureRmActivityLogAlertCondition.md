---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430249"
---
# <span data-ttu-id="45412-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="45412-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="45412-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45412-102">SYNOPSIS</span></span>
<span data-ttu-id="45412-103">Cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="45412-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45412-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45412-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45412-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45412-105">DESCRIPTION</span></span>
<span data-ttu-id="45412-106">O cmdlet **New-AzureRmActivityLogAlertCondition** cria novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="45412-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="45412-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45412-107">EXAMPLES</span></span>

### <span data-ttu-id="45412-108">Exemplo 1: criar um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="45412-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="45412-109">Esse comando cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="45412-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="45412-110">**Observação** : quando esse cmdlet é usado com Set-AzureRmActivityLogAlert pelo menos um desses objetos, passados como parâmetros, deve ter seu campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="45412-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="45412-111">Caso contrário, o back-end responderá com um 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="45412-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="45412-112">OS</span><span class="sxs-lookup"><span data-stu-id="45412-112">PARAMETERS</span></span>

### <span data-ttu-id="45412-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45412-113">-DefaultProfile</span></span>
<span data-ttu-id="45412-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="45412-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45412-115">-Igual</span><span class="sxs-lookup"><span data-stu-id="45412-115">-Equal</span></span>
<span data-ttu-id="45412-116">Especifica a propriedade Equals para a condição de folha.</span><span class="sxs-lookup"><span data-stu-id="45412-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="45412-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="45412-117">-Field</span></span>
<span data-ttu-id="45412-118">Especifica o campo para a condição.</span><span class="sxs-lookup"><span data-stu-id="45412-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="45412-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45412-119">CommonParameters</span></span>
<span data-ttu-id="45412-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45412-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45412-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45412-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45412-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45412-122">INPUTS</span></span>

### <span data-ttu-id="45412-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45412-123">System.String</span></span>

## <span data-ttu-id="45412-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45412-124">OUTPUTS</span></span>

### <span data-ttu-id="45412-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="45412-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="45412-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45412-126">NOTES</span></span>

## <span data-ttu-id="45412-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45412-127">RELATED LINKS</span></span>

[<span data-ttu-id="45412-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45412-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="45412-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45412-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="45412-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45412-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="45412-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45412-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="45412-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45412-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="45412-133">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="45412-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
