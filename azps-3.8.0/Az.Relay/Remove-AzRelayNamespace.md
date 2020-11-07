---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778150"
---
# <span data-ttu-id="b4583-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="b4583-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="b4583-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4583-102">SYNOPSIS</span></span>
<span data-ttu-id="b4583-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b4583-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="b4583-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4583-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4583-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4583-105">DESCRIPTION</span></span>
<span data-ttu-id="b4583-106">O cmdlet **Remove-AzRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b4583-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="b4583-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4583-107">EXAMPLES</span></span>

### <span data-ttu-id="b4583-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4583-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="b4583-109">Remove o namespace de retransmissão `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="b4583-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="b4583-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4583-110">PARAMETERS</span></span>

### <span data-ttu-id="b4583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4583-111">-DefaultProfile</span></span>
<span data-ttu-id="b4583-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4583-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4583-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4583-113">-Name</span></span>
<span data-ttu-id="b4583-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="b4583-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="b4583-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4583-115">-ResourceGroupName</span></span>
<span data-ttu-id="b4583-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4583-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4583-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4583-117">-Confirm</span></span>
<span data-ttu-id="b4583-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4583-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4583-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4583-119">-WhatIf</span></span>
<span data-ttu-id="b4583-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4583-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4583-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4583-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4583-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4583-122">CommonParameters</span></span>
<span data-ttu-id="b4583-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4583-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4583-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4583-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4583-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4583-125">INPUTS</span></span>

### <span data-ttu-id="b4583-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b4583-126">System.String</span></span>

## <span data-ttu-id="b4583-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4583-127">OUTPUTS</span></span>

### <span data-ttu-id="b4583-128">System. void</span><span class="sxs-lookup"><span data-stu-id="b4583-128">System.Void</span></span>

## <span data-ttu-id="b4583-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4583-129">NOTES</span></span>

## <span data-ttu-id="b4583-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4583-130">RELATED LINKS</span></span>
