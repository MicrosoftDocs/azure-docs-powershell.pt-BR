---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112634"
---
# <span data-ttu-id="f5f89-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f5f89-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f5f89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5f89-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f89-103">Adiciona uma assinatura a um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f5f89-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f5f89-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5f89-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f89-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5f89-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f89-106">O cmdlet **New-AzManagementGroupSubscription** adiciona uma Assinatura a um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f5f89-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f5f89-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5f89-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f89-108">Exemplo 1: Adicionar Assinatura a um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f5f89-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f5f89-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5f89-109">PARAMETERS</span></span>

### <span data-ttu-id="f5f89-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f89-110">-DefaultProfile</span></span>
<span data-ttu-id="f5f89-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f89-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f89-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f5f89-112">-GroupName</span></span>
<span data-ttu-id="f5f89-113">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f5f89-113">Management Group Id</span></span>

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

### <span data-ttu-id="f5f89-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5f89-114">-PassThru</span></span>
<span data-ttu-id="f5f89-115">Retornar `true` após a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="f5f89-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f5f89-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5f89-116">-SubscriptionId</span></span>
<span data-ttu-id="f5f89-117">ID da assinatura associada ao gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f5f89-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="f5f89-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5f89-118">-Confirm</span></span>
<span data-ttu-id="f5f89-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f89-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f89-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f89-120">-WhatIf</span></span>
<span data-ttu-id="f5f89-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5f89-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f89-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5f89-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f89-123">CommonParameters</span></span>
<span data-ttu-id="f5f89-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f89-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5f89-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f89-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5f89-126">INPUTS</span></span>

### <span data-ttu-id="f5f89-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5f89-127">None</span></span>

## <span data-ttu-id="f5f89-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5f89-128">OUTPUTS</span></span>

### <span data-ttu-id="f5f89-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5f89-129">System.Boolean</span></span>

## <span data-ttu-id="f5f89-130">Notas</span><span class="sxs-lookup"><span data-stu-id="f5f89-130">NOTES</span></span>

## <span data-ttu-id="f5f89-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5f89-131">RELATED LINKS</span></span>
