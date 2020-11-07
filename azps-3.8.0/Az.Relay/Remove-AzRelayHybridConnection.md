---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778154"
---
# <span data-ttu-id="ac581-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ac581-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ac581-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac581-102">SYNOPSIS</span></span>
<span data-ttu-id="ac581-103">Remove o HybridConnection do namespace HybridConnection especificado.</span><span class="sxs-lookup"><span data-stu-id="ac581-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="ac581-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac581-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac581-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac581-105">DESCRIPTION</span></span>
<span data-ttu-id="ac581-106">O cmdlet **Remove-AzRelayHybridConnection** remove o HybridConnection do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="ac581-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="ac581-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac581-107">EXAMPLES</span></span>

### <span data-ttu-id="ac581-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac581-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="ac581-109">Remove o HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ac581-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ac581-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac581-110">PARAMETERS</span></span>

### <span data-ttu-id="ac581-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac581-111">-DefaultProfile</span></span>
<span data-ttu-id="ac581-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac581-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac581-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac581-113">-Name</span></span>
<span data-ttu-id="ac581-114">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="ac581-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ac581-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac581-115">-Namespace</span></span>
<span data-ttu-id="ac581-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="ac581-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ac581-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac581-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac581-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac581-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="ac581-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac581-119">-Confirm</span></span>
<span data-ttu-id="ac581-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac581-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac581-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac581-121">-WhatIf</span></span>
<span data-ttu-id="ac581-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac581-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac581-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac581-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac581-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac581-124">CommonParameters</span></span>
<span data-ttu-id="ac581-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac581-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac581-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac581-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac581-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac581-127">INPUTS</span></span>

### <span data-ttu-id="ac581-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac581-128">System.String</span></span>

## <span data-ttu-id="ac581-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac581-129">OUTPUTS</span></span>

### <span data-ttu-id="ac581-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ac581-130">System.Void</span></span>

## <span data-ttu-id="ac581-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac581-131">NOTES</span></span>

## <span data-ttu-id="ac581-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac581-132">RELATED LINKS</span></span>
