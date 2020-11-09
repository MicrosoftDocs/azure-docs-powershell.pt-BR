---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283800"
---
# <span data-ttu-id="5c657-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="5c657-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="5c657-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c657-102">SYNOPSIS</span></span>
<span data-ttu-id="5c657-103">Remove o HybridConnection do namespace HybridConnection especificado.</span><span class="sxs-lookup"><span data-stu-id="5c657-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="5c657-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c657-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c657-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c657-105">DESCRIPTION</span></span>
<span data-ttu-id="5c657-106">O cmdlet **Remove-AzRelayHybridConnection** remove o HybridConnection do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="5c657-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="5c657-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c657-107">EXAMPLES</span></span>

### <span data-ttu-id="5c657-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c657-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="5c657-109">Remove o HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="5c657-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5c657-110">OS</span><span class="sxs-lookup"><span data-stu-id="5c657-110">PARAMETERS</span></span>

### <span data-ttu-id="5c657-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c657-111">-DefaultProfile</span></span>
<span data-ttu-id="5c657-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c657-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c657-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c657-113">-Name</span></span>
<span data-ttu-id="5c657-114">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="5c657-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="5c657-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c657-115">-Namespace</span></span>
<span data-ttu-id="5c657-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="5c657-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5c657-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c657-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c657-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c657-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c657-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c657-119">-Confirm</span></span>
<span data-ttu-id="5c657-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c657-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c657-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c657-121">-WhatIf</span></span>
<span data-ttu-id="5c657-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c657-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c657-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c657-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c657-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c657-124">CommonParameters</span></span>
<span data-ttu-id="5c657-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c657-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c657-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c657-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c657-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c657-127">INPUTS</span></span>

### <span data-ttu-id="5c657-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5c657-128">System.String</span></span>

## <span data-ttu-id="5c657-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c657-129">OUTPUTS</span></span>

### <span data-ttu-id="5c657-130">System. void</span><span class="sxs-lookup"><span data-stu-id="5c657-130">System.Void</span></span>

## <span data-ttu-id="5c657-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c657-131">NOTES</span></span>

## <span data-ttu-id="5c657-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c657-132">RELATED LINKS</span></span>
