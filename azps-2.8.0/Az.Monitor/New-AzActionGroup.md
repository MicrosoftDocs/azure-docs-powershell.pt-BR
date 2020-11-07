---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 1377e1fe5f96754f4b20858cc1930039246bd8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771881"
---
# <span data-ttu-id="04d18-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="04d18-101">New-AzActionGroup</span></span>

## <span data-ttu-id="04d18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04d18-102">SYNOPSIS</span></span>
<span data-ttu-id="04d18-103">Cria um objeto de referência do objeto de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="04d18-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="04d18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04d18-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04d18-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04d18-105">DESCRIPTION</span></span>
<span data-ttu-id="04d18-106">O cmdlet **New-AzActionGroup** cria um objeto de referência de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="04d18-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="04d18-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04d18-107">EXAMPLES</span></span>

### <span data-ttu-id="04d18-108">Exemplo 1: criar um objeto de referência do grupo de ação na memória</span><span class="sxs-lookup"><span data-stu-id="04d18-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="04d18-109">OS</span><span class="sxs-lookup"><span data-stu-id="04d18-109">PARAMETERS</span></span>

### <span data-ttu-id="04d18-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="04d18-110">-ActionGroupId</span></span>
<span data-ttu-id="04d18-111">A ID/nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="04d18-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="04d18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d18-112">-DefaultProfile</span></span>
<span data-ttu-id="04d18-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04d18-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04d18-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="04d18-114">-WebhookProperty</span></span>
<span data-ttu-id="04d18-115">As propriedades do webhook do grupo ação</span><span class="sxs-lookup"><span data-stu-id="04d18-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="04d18-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d18-116">CommonParameters</span></span>
<span data-ttu-id="04d18-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d18-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d18-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04d18-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d18-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04d18-119">INPUTS</span></span>

### <span data-ttu-id="04d18-120">System. String</span><span class="sxs-lookup"><span data-stu-id="04d18-120">System.String</span></span>

### <span data-ttu-id="04d18-121">System. Collections. Generic. Dictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04d18-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04d18-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04d18-122">OUTPUTS</span></span>

### <span data-ttu-id="04d18-123">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="04d18-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="04d18-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04d18-124">NOTES</span></span>

## <span data-ttu-id="04d18-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04d18-125">RELATED LINKS</span></span>

[<span data-ttu-id="04d18-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04d18-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="04d18-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04d18-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="04d18-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04d18-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="04d18-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04d18-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="04d18-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04d18-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="04d18-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="04d18-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
