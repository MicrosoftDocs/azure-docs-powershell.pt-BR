---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: ecd5771478f3d3ff3cee4a5045d6c72eb707af11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890583"
---
# <span data-ttu-id="028c6-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="028c6-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="028c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="028c6-102">SYNOPSIS</span></span>
<span data-ttu-id="028c6-103">Adiciona uma assinatura a um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="028c6-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="028c6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="028c6-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="028c6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="028c6-105">DESCRIPTION</span></span>
<span data-ttu-id="028c6-106">O cmdlet **New-AzManagementGroupSubscription** adiciona uma Assinatura a um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="028c6-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="028c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="028c6-107">EXAMPLES</span></span>

### <span data-ttu-id="028c6-108">Exemplo 1: Adicionar Assinatura a um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="028c6-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="028c6-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="028c6-109">PARAMETERS</span></span>

### <span data-ttu-id="028c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028c6-110">-DefaultProfile</span></span>
<span data-ttu-id="028c6-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="028c6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="028c6-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="028c6-112">-GroupName</span></span>
<span data-ttu-id="028c6-113">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="028c6-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028c6-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="028c6-114">-PassThru</span></span>
<span data-ttu-id="028c6-115">Retornar `true` a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="028c6-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028c6-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="028c6-116">-SubscriptionId</span></span>
<span data-ttu-id="028c6-117">ID de assinatura da assinatura associada ao gerenciamento</span><span class="sxs-lookup"><span data-stu-id="028c6-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028c6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="028c6-118">-Confirm</span></span>
<span data-ttu-id="028c6-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="028c6-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028c6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="028c6-120">-WhatIf</span></span>
<span data-ttu-id="028c6-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="028c6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="028c6-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="028c6-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028c6-123">CommonParameters</span></span>
<span data-ttu-id="028c6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028c6-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="028c6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028c6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="028c6-126">INPUTS</span></span>

### <span data-ttu-id="028c6-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="028c6-127">None</span></span>

## <span data-ttu-id="028c6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="028c6-128">OUTPUTS</span></span>

### <span data-ttu-id="028c6-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="028c6-129">System.Boolean</span></span>

## <span data-ttu-id="028c6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="028c6-130">NOTES</span></span>

## <span data-ttu-id="028c6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="028c6-131">RELATED LINKS</span></span>
