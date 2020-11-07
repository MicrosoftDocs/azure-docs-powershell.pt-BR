---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785250"
---
# <span data-ttu-id="cbaa6-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="cbaa6-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="cbaa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbaa6-103">Cria um objeto de referência do objeto de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="cbaa6-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbaa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbaa6-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbaa6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbaa6-105">DESCRIPTION</span></span>
<span data-ttu-id="cbaa6-106">O cmdlet **New-AzureRmActionGroup** cria um objeto de referência de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="cbaa6-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="cbaa6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbaa6-107">EXAMPLES</span></span>

### <span data-ttu-id="cbaa6-108">Exemplo 1: criar um objeto de referência do grupo de ação na memória</span><span class="sxs-lookup"><span data-stu-id="cbaa6-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="cbaa6-109">OS</span><span class="sxs-lookup"><span data-stu-id="cbaa6-109">PARAMETERS</span></span>

### <span data-ttu-id="cbaa6-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="cbaa6-110">-ActionGroupId</span></span>
<span data-ttu-id="cbaa6-111">A ID/nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="cbaa6-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="cbaa6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbaa6-112">-DefaultProfile</span></span>
<span data-ttu-id="cbaa6-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cbaa6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbaa6-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="cbaa6-114">-WebhookProperty</span></span>
<span data-ttu-id="cbaa6-115">As propriedades do webhook do grupo ação</span><span class="sxs-lookup"><span data-stu-id="cbaa6-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="cbaa6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbaa6-116">CommonParameters</span></span>
<span data-ttu-id="cbaa6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbaa6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbaa6-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbaa6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbaa6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbaa6-119">INPUTS</span></span>

### <span data-ttu-id="cbaa6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="cbaa6-120">System.String</span></span>

### <span data-ttu-id="cbaa6-121">System. Collections. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cbaa6-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cbaa6-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbaa6-122">OUTPUTS</span></span>

### <span data-ttu-id="cbaa6-123">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="cbaa6-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="cbaa6-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbaa6-124">NOTES</span></span>

## <span data-ttu-id="cbaa6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbaa6-125">RELATED LINKS</span></span>

[<span data-ttu-id="cbaa6-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cbaa6-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cbaa6-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cbaa6-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cbaa6-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cbaa6-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cbaa6-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cbaa6-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cbaa6-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cbaa6-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cbaa6-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="cbaa6-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

