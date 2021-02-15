---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 48ddcf7c6bed9e31bec486eaaa433c35eaed0fe3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399015"
---
# <span data-ttu-id="987f1-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="987f1-101">New-AzActionGroup</span></span>

## <span data-ttu-id="987f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="987f1-102">SYNOPSIS</span></span>
<span data-ttu-id="987f1-103">Cria um objeto de referência ActionGroup na memória.</span><span class="sxs-lookup"><span data-stu-id="987f1-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="987f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="987f1-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987f1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="987f1-105">DESCRIPTION</span></span>
<span data-ttu-id="987f1-106">O **cmdlet New-AzActionGroup** cria um objeto de referência de grupo de ações na memória.</span><span class="sxs-lookup"><span data-stu-id="987f1-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="987f1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="987f1-107">EXAMPLES</span></span>

### <span data-ttu-id="987f1-108">Exemplo 1: Criar um objeto de referência de grupo de ações na memória</span><span class="sxs-lookup"><span data-stu-id="987f1-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="987f1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="987f1-109">PARAMETERS</span></span>

### <span data-ttu-id="987f1-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="987f1-110">-ActionGroupId</span></span>
<span data-ttu-id="987f1-111">A ID/nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="987f1-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="987f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987f1-112">-DefaultProfile</span></span>
<span data-ttu-id="987f1-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="987f1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="987f1-114">-WebertProperty</span><span class="sxs-lookup"><span data-stu-id="987f1-114">-WebhookProperty</span></span>
<span data-ttu-id="987f1-115">As propriedades web browser do grupo de ações</span><span class="sxs-lookup"><span data-stu-id="987f1-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="987f1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987f1-116">CommonParameters</span></span>
<span data-ttu-id="987f1-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987f1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987f1-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="987f1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987f1-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="987f1-119">INPUTS</span></span>

### <span data-ttu-id="987f1-120">System.String</span><span class="sxs-lookup"><span data-stu-id="987f1-120">System.String</span></span>

### <span data-ttu-id="987f1-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="987f1-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="987f1-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="987f1-122">OUTPUTS</span></span>

### <span data-ttu-id="987f1-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="987f1-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="987f1-124">Notas</span><span class="sxs-lookup"><span data-stu-id="987f1-124">NOTES</span></span>

## <span data-ttu-id="987f1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="987f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="987f1-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="987f1-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="987f1-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="987f1-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="987f1-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="987f1-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="987f1-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="987f1-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="987f1-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="987f1-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



