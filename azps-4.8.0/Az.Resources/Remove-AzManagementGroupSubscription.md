---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110953"
---
# <span data-ttu-id="f9d80-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f9d80-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f9d80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9d80-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d80-103">Remove uma assinatura de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f9d80-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f9d80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9d80-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d80-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9d80-105">DESCRIPTION</span></span>
<span data-ttu-id="f9d80-106">O cmdlet **Remove-AzManagementGroupSubscription** remove uma assinatura de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f9d80-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f9d80-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9d80-107">EXAMPLES</span></span>

### <span data-ttu-id="f9d80-108">Exemplo 1: remover a assinatura de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f9d80-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f9d80-109">OS</span><span class="sxs-lookup"><span data-stu-id="f9d80-109">PARAMETERS</span></span>

### <span data-ttu-id="f9d80-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d80-110">-DefaultProfile</span></span>
<span data-ttu-id="f9d80-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d80-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d80-112">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="f9d80-112">-GroupName</span></span>
<span data-ttu-id="f9d80-113">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f9d80-113">Management Group Id</span></span>

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

### <span data-ttu-id="f9d80-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9d80-114">-PassThru</span></span>
<span data-ttu-id="f9d80-115">Retorno `true` sobre a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="f9d80-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f9d80-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9d80-116">-SubscriptionId</span></span>
<span data-ttu-id="f9d80-117">ID da assinatura associada ao gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f9d80-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="f9d80-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9d80-118">-Confirm</span></span>
<span data-ttu-id="f9d80-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d80-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d80-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d80-120">-WhatIf</span></span>
<span data-ttu-id="f9d80-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9d80-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d80-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9d80-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d80-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d80-123">CommonParameters</span></span>
<span data-ttu-id="f9d80-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d80-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d80-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9d80-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d80-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9d80-126">INPUTS</span></span>

### <span data-ttu-id="f9d80-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f9d80-127">None</span></span>

## <span data-ttu-id="f9d80-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9d80-128">OUTPUTS</span></span>

### <span data-ttu-id="f9d80-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9d80-129">System.Boolean</span></span>

## <span data-ttu-id="f9d80-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9d80-130">NOTES</span></span>

## <span data-ttu-id="f9d80-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9d80-131">RELATED LINKS</span></span>
