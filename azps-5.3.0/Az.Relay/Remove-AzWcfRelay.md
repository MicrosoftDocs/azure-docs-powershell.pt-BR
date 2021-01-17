---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428023"
---
# <span data-ttu-id="d843b-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d843b-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="d843b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d843b-102">SYNOPSIS</span></span>
<span data-ttu-id="d843b-103">Remove o WcfRelay do namespace especificado de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="d843b-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="d843b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d843b-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d843b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d843b-105">DESCRIPTION</span></span>
<span data-ttu-id="d843b-106">O cmdlet **Remove-AzWcfRelay** remove o WcfRelay do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="d843b-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="d843b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d843b-107">EXAMPLES</span></span>

### <span data-ttu-id="d843b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d843b-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="d843b-109">Remove o WcfRelay `TestWCFRelay1` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d843b-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d843b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d843b-110">PARAMETERS</span></span>

### <span data-ttu-id="d843b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d843b-111">-DefaultProfile</span></span>
<span data-ttu-id="d843b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d843b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d843b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d843b-113">-Name</span></span>
<span data-ttu-id="d843b-114">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="d843b-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d843b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d843b-115">-Namespace</span></span>
<span data-ttu-id="d843b-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="d843b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="d843b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d843b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d843b-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d843b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d843b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d843b-119">-Confirm</span></span>
<span data-ttu-id="d843b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d843b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d843b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d843b-121">-WhatIf</span></span>
<span data-ttu-id="d843b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d843b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d843b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d843b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d843b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d843b-124">CommonParameters</span></span>
<span data-ttu-id="d843b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d843b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d843b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d843b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d843b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d843b-127">INPUTS</span></span>

### <span data-ttu-id="d843b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d843b-128">System.String</span></span>

## <span data-ttu-id="d843b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d843b-129">OUTPUTS</span></span>

### <span data-ttu-id="d843b-130">System. void</span><span class="sxs-lookup"><span data-stu-id="d843b-130">System.Void</span></span>

## <span data-ttu-id="d843b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d843b-131">NOTES</span></span>

## <span data-ttu-id="d843b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d843b-132">RELATED LINKS</span></span>
