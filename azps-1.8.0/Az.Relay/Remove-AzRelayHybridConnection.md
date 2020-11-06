---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b0d7ef4a3fcaf681ea52719a5c7627784dac8d65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599502"
---
# <span data-ttu-id="4fcbe-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="4fcbe-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="4fcbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcbe-103">Remove o HybridConnection do namespace HybridConnection especificado.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="4fcbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fcbe-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fcbe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="4fcbe-106">O cmdlet **Remove-AzRelayHybridConnection** remove o HybridConnection do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="4fcbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fcbe-107">EXAMPLES</span></span>

### <span data-ttu-id="4fcbe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fcbe-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="4fcbe-109">Remove o HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4fcbe-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4fcbe-110">OS</span><span class="sxs-lookup"><span data-stu-id="4fcbe-110">PARAMETERS</span></span>

### <span data-ttu-id="4fcbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcbe-111">-DefaultProfile</span></span>
<span data-ttu-id="4fcbe-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fcbe-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fcbe-113">-Name</span></span>
<span data-ttu-id="4fcbe-114">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="4fcbe-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4fcbe-115">-Namespace</span></span>
<span data-ttu-id="4fcbe-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4fcbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="4fcbe-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4fcbe-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fcbe-119">-Confirm</span></span>
<span data-ttu-id="4fcbe-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fcbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fcbe-121">-WhatIf</span></span>
<span data-ttu-id="4fcbe-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fcbe-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fcbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcbe-124">CommonParameters</span></span>
<span data-ttu-id="4fcbe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fcbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcbe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fcbe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcbe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fcbe-127">INPUTS</span></span>

### <span data-ttu-id="4fcbe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4fcbe-128">System.String</span></span>

## <span data-ttu-id="4fcbe-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fcbe-129">OUTPUTS</span></span>

### <span data-ttu-id="4fcbe-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4fcbe-130">System.Void</span></span>

## <span data-ttu-id="4fcbe-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fcbe-131">NOTES</span></span>

## <span data-ttu-id="4fcbe-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fcbe-132">RELATED LINKS</span></span>
