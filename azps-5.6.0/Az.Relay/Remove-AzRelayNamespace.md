---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891709"
---
# <span data-ttu-id="a4bce-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a4bce-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="a4bce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4bce-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bce-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a4bce-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="a4bce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4bce-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4bce-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4bce-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bce-106">O cmdlet **Remove-AzRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a4bce-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="a4bce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4bce-107">EXAMPLES</span></span>

### <span data-ttu-id="a4bce-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4bce-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="a4bce-109">Remove o namespace Relay `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="a4bce-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="a4bce-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4bce-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bce-111">-DefaultProfile</span></span>
<span data-ttu-id="a4bce-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4bce-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a4bce-113">-Name</span></span>
<span data-ttu-id="a4bce-114">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="a4bce-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a4bce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bce-115">-ResourceGroupName</span></span>
<span data-ttu-id="a4bce-116">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a4bce-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4bce-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4bce-117">-Confirm</span></span>
<span data-ttu-id="a4bce-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4bce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4bce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4bce-119">-WhatIf</span></span>
<span data-ttu-id="a4bce-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4bce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4bce-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4bce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4bce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bce-122">CommonParameters</span></span>
<span data-ttu-id="a4bce-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bce-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bce-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4bce-125">INPUTS</span></span>

### <span data-ttu-id="a4bce-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a4bce-126">System.String</span></span>

## <span data-ttu-id="a4bce-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4bce-127">OUTPUTS</span></span>

### <span data-ttu-id="a4bce-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="a4bce-128">System.Void</span></span>

## <span data-ttu-id="a4bce-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4bce-129">NOTES</span></span>

## <span data-ttu-id="a4bce-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4bce-130">RELATED LINKS</span></span>
