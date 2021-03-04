---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 79960e61b6b414458c6c41cea9e6cd550097d022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888875"
---
# <span data-ttu-id="cfe65-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="cfe65-101">New-AzActionGroup</span></span>

## <span data-ttu-id="cfe65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe65-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe65-103">Cria um objeto de referência ActionGroup na memória.</span><span class="sxs-lookup"><span data-stu-id="cfe65-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="cfe65-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cfe65-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfe65-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cfe65-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe65-106">O cmdlet **New-AzActionGroup** cria um objeto de referência do grupo de ações na memória.</span><span class="sxs-lookup"><span data-stu-id="cfe65-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="cfe65-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfe65-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe65-108">Exemplo 1: Criar um objeto de referência de grupo de ações na memória</span><span class="sxs-lookup"><span data-stu-id="cfe65-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="cfe65-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cfe65-109">PARAMETERS</span></span>

### <span data-ttu-id="cfe65-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="cfe65-110">-ActionGroupId</span></span>
<span data-ttu-id="cfe65-111">A Id/nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="cfe65-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="cfe65-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe65-112">-DefaultProfile</span></span>
<span data-ttu-id="cfe65-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cfe65-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfe65-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="cfe65-114">-WebhookProperty</span></span>
<span data-ttu-id="cfe65-115">As propriedades de webhook do grupo de ações</span><span class="sxs-lookup"><span data-stu-id="cfe65-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="cfe65-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe65-116">CommonParameters</span></span>
<span data-ttu-id="cfe65-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe65-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe65-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfe65-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe65-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfe65-119">INPUTS</span></span>

### <span data-ttu-id="cfe65-120">System.String</span><span class="sxs-lookup"><span data-stu-id="cfe65-120">System.String</span></span>

### <span data-ttu-id="cfe65-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cfe65-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cfe65-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cfe65-122">OUTPUTS</span></span>

### <span data-ttu-id="cfe65-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="cfe65-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="cfe65-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="cfe65-124">NOTES</span></span>

## <span data-ttu-id="cfe65-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfe65-125">RELATED LINKS</span></span>

[<span data-ttu-id="cfe65-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfe65-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="cfe65-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfe65-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="cfe65-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfe65-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="cfe65-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfe65-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="cfe65-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfe65-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="cfe65-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="cfe65-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

