---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f523f0d1166a40e04ac85344c0fc96640a140bb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773389"
---
# <span data-ttu-id="3b2f3-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="3b2f3-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="3b2f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2f3-103">Remove o WcfRelay do namespace especificado de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="3b2f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b2f3-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b2f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3b2f3-106">O cmdlet **Remove-AzWcfRelay** remove o WcfRelay do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="3b2f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b2f3-107">EXAMPLES</span></span>

### <span data-ttu-id="3b2f3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b2f3-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="3b2f3-109">Remove o WcfRelay `TestWCFRelay1` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="3b2f3-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="3b2f3-110">OS</span><span class="sxs-lookup"><span data-stu-id="3b2f3-110">PARAMETERS</span></span>

### <span data-ttu-id="3b2f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2f3-111">-DefaultProfile</span></span>
<span data-ttu-id="3b2f3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b2f3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b2f3-113">-Name</span></span>
<span data-ttu-id="3b2f3-114">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3b2f3-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b2f3-115">-Namespace</span></span>
<span data-ttu-id="3b2f3-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-116">Namespace Name.</span></span>

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

### <span data-ttu-id="3b2f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b2f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b2f3-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3b2f3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b2f3-119">-Confirm</span></span>
<span data-ttu-id="3b2f3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b2f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b2f3-121">-WhatIf</span></span>
<span data-ttu-id="3b2f3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b2f3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b2f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2f3-124">CommonParameters</span></span>
<span data-ttu-id="3b2f3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b2f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2f3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2f3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b2f3-127">INPUTS</span></span>

### <span data-ttu-id="3b2f3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3b2f3-128">System.String</span></span>

## <span data-ttu-id="3b2f3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b2f3-129">OUTPUTS</span></span>

### <span data-ttu-id="3b2f3-130">System. void</span><span class="sxs-lookup"><span data-stu-id="3b2f3-130">System.Void</span></span>

## <span data-ttu-id="3b2f3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b2f3-131">NOTES</span></span>

## <span data-ttu-id="3b2f3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b2f3-132">RELATED LINKS</span></span>