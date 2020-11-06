---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603375"
---
# <span data-ttu-id="c5bf6-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="c5bf6-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="c5bf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bf6-103">Cria um objeto de referência do objeto de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="c5bf6-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5bf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5bf6-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5bf6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bf6-106">O cmdlet **New-AzureRmActionGroup** cria um objeto de referência de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="c5bf6-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="c5bf6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bf6-108">Exemplo 1: criar um objeto de referência do grupo de ação na memória</span><span class="sxs-lookup"><span data-stu-id="c5bf6-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="c5bf6-109">OS</span><span class="sxs-lookup"><span data-stu-id="c5bf6-109">PARAMETERS</span></span>

### <span data-ttu-id="c5bf6-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c5bf6-110">-ActionGroupId</span></span>
<span data-ttu-id="c5bf6-111">A ID/nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="c5bf6-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="c5bf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bf6-112">-DefaultProfile</span></span>
<span data-ttu-id="c5bf6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bf6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bf6-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="c5bf6-114">-WebhookProperty</span></span>
<span data-ttu-id="c5bf6-115">As propriedades do webhook do grupo ação</span><span class="sxs-lookup"><span data-stu-id="c5bf6-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bf6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bf6-116">CommonParameters</span></span>
<span data-ttu-id="c5bf6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bf6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bf6-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bf6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bf6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5bf6-119">INPUTS</span></span>

## <span data-ttu-id="c5bf6-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5bf6-120">OUTPUTS</span></span>

### <span data-ttu-id="c5bf6-121">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="c5bf6-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="c5bf6-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5bf6-122">NOTES</span></span>

## <span data-ttu-id="c5bf6-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5bf6-123">RELATED LINKS</span></span>

[<span data-ttu-id="c5bf6-124">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5bf6-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5bf6-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5bf6-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5bf6-126">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5bf6-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5bf6-127">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5bf6-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5bf6-128">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5bf6-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5bf6-129">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="c5bf6-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

