---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f99a3a999baad580e04c6872f047c02d4a99091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891706"
---
# <span data-ttu-id="36162-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="36162-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="36162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36162-102">SYNOPSIS</span></span>
<span data-ttu-id="36162-103">Remove o WcfRelay do namespace Relay especificado.</span><span class="sxs-lookup"><span data-stu-id="36162-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="36162-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36162-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36162-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36162-105">DESCRIPTION</span></span>
<span data-ttu-id="36162-106">O cmdlet **Remove-AzWcfRelay** remove o WcfRelay do namespace Relay especificado.</span><span class="sxs-lookup"><span data-stu-id="36162-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="36162-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36162-107">EXAMPLES</span></span>

### <span data-ttu-id="36162-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36162-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="36162-109">Remove o WcfRelay `TestWCFRelay1` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="36162-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="36162-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36162-110">PARAMETERS</span></span>

### <span data-ttu-id="36162-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36162-111">-DefaultProfile</span></span>
<span data-ttu-id="36162-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36162-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36162-113">-Name</span><span class="sxs-lookup"><span data-stu-id="36162-113">-Name</span></span>
<span data-ttu-id="36162-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="36162-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36162-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36162-115">-Namespace</span></span>
<span data-ttu-id="36162-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="36162-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36162-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36162-117">-ResourceGroupName</span></span>
<span data-ttu-id="36162-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="36162-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36162-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36162-119">-Confirm</span></span>
<span data-ttu-id="36162-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36162-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36162-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36162-121">-WhatIf</span></span>
<span data-ttu-id="36162-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36162-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36162-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36162-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36162-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36162-124">CommonParameters</span></span>
<span data-ttu-id="36162-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36162-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36162-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36162-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36162-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36162-127">INPUTS</span></span>

### <span data-ttu-id="36162-128">System.String</span><span class="sxs-lookup"><span data-stu-id="36162-128">System.String</span></span>

## <span data-ttu-id="36162-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36162-129">OUTPUTS</span></span>

### <span data-ttu-id="36162-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="36162-130">System.Void</span></span>

## <span data-ttu-id="36162-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="36162-131">NOTES</span></span>

## <span data-ttu-id="36162-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36162-132">RELATED LINKS</span></span>
