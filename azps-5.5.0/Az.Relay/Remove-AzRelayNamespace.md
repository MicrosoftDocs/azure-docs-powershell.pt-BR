---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116217"
---
# <span data-ttu-id="32370-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="32370-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="32370-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32370-102">SYNOPSIS</span></span>
<span data-ttu-id="32370-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="32370-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="32370-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32370-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32370-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="32370-105">DESCRIPTION</span></span>
<span data-ttu-id="32370-106">O **cmdlet Remove-AzRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="32370-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="32370-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32370-107">EXAMPLES</span></span>

### <span data-ttu-id="32370-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32370-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="32370-109">Remove o namespace relay `TestNameSpace-Relay1` do grupo de recursos `Default-ServiceBus-WestUS` especificado.</span><span class="sxs-lookup"><span data-stu-id="32370-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="32370-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32370-110">PARAMETERS</span></span>

### <span data-ttu-id="32370-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32370-111">-DefaultProfile</span></span>
<span data-ttu-id="32370-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32370-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32370-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="32370-113">-Name</span></span>
<span data-ttu-id="32370-114">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="32370-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="32370-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32370-115">-ResourceGroupName</span></span>
<span data-ttu-id="32370-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32370-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="32370-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="32370-117">-Confirm</span></span>
<span data-ttu-id="32370-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32370-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32370-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32370-119">-WhatIf</span></span>
<span data-ttu-id="32370-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="32370-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32370-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32370-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32370-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32370-122">CommonParameters</span></span>
<span data-ttu-id="32370-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32370-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32370-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32370-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32370-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="32370-125">INPUTS</span></span>

### <span data-ttu-id="32370-126">System.String</span><span class="sxs-lookup"><span data-stu-id="32370-126">System.String</span></span>

## <span data-ttu-id="32370-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="32370-127">OUTPUTS</span></span>

### <span data-ttu-id="32370-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="32370-128">System.Void</span></span>

## <span data-ttu-id="32370-129">Notas</span><span class="sxs-lookup"><span data-stu-id="32370-129">NOTES</span></span>

## <span data-ttu-id="32370-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32370-130">RELATED LINKS</span></span>
