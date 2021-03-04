---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b426eda2ab7e9714cd46a95c25d248adef5464a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891710"
---
# <span data-ttu-id="67696-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="67696-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="67696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67696-102">SYNOPSIS</span></span>
<span data-ttu-id="67696-103">Remove o HybridConnection do namespace HybridConnection especificado.</span><span class="sxs-lookup"><span data-stu-id="67696-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="67696-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67696-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67696-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67696-105">DESCRIPTION</span></span>
<span data-ttu-id="67696-106">O cmdlet **Remove-AzRelayHybridConnection** remove o HybridConnection do namespace Relay especificado.</span><span class="sxs-lookup"><span data-stu-id="67696-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="67696-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67696-107">EXAMPLES</span></span>

### <span data-ttu-id="67696-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67696-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="67696-109">Remove o HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="67696-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="67696-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67696-110">PARAMETERS</span></span>

### <span data-ttu-id="67696-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67696-111">-DefaultProfile</span></span>
<span data-ttu-id="67696-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67696-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67696-113">-Name</span><span class="sxs-lookup"><span data-stu-id="67696-113">-Name</span></span>
<span data-ttu-id="67696-114">Nome de HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="67696-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="67696-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67696-115">-Namespace</span></span>
<span data-ttu-id="67696-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="67696-116">Namespace Name.</span></span>

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

### <span data-ttu-id="67696-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67696-117">-ResourceGroupName</span></span>
<span data-ttu-id="67696-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="67696-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="67696-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67696-119">-Confirm</span></span>
<span data-ttu-id="67696-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67696-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67696-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67696-121">-WhatIf</span></span>
<span data-ttu-id="67696-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67696-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67696-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67696-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67696-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67696-124">CommonParameters</span></span>
<span data-ttu-id="67696-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67696-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67696-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67696-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67696-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67696-127">INPUTS</span></span>

### <span data-ttu-id="67696-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67696-128">System.String</span></span>

## <span data-ttu-id="67696-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67696-129">OUTPUTS</span></span>

### <span data-ttu-id="67696-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="67696-130">System.Void</span></span>

## <span data-ttu-id="67696-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="67696-131">NOTES</span></span>

## <span data-ttu-id="67696-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67696-132">RELATED LINKS</span></span>
