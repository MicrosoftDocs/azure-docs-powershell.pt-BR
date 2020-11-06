---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: dec858fe113725876e7e46d72cf996d9338b34eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599500"
---
# <span data-ttu-id="a9996-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a9996-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="a9996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9996-102">SYNOPSIS</span></span>
<span data-ttu-id="a9996-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a9996-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="a9996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9996-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9996-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9996-105">DESCRIPTION</span></span>
<span data-ttu-id="a9996-106">O cmdlet **Remove-AzRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a9996-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="a9996-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9996-107">EXAMPLES</span></span>

### <span data-ttu-id="a9996-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9996-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="a9996-109">Remove o namespace de retransmissão `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="a9996-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="a9996-110">OS</span><span class="sxs-lookup"><span data-stu-id="a9996-110">PARAMETERS</span></span>

### <span data-ttu-id="a9996-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9996-111">-DefaultProfile</span></span>
<span data-ttu-id="a9996-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9996-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9996-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9996-113">-Name</span></span>
<span data-ttu-id="a9996-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="a9996-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a9996-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9996-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9996-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9996-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="a9996-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9996-117">-Confirm</span></span>
<span data-ttu-id="a9996-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9996-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9996-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9996-119">-WhatIf</span></span>
<span data-ttu-id="a9996-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9996-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9996-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9996-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9996-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9996-122">CommonParameters</span></span>
<span data-ttu-id="a9996-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9996-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9996-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9996-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9996-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9996-125">INPUTS</span></span>

### <span data-ttu-id="a9996-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a9996-126">System.String</span></span>

## <span data-ttu-id="a9996-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9996-127">OUTPUTS</span></span>

### <span data-ttu-id="a9996-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a9996-128">System.Void</span></span>

## <span data-ttu-id="a9996-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9996-129">NOTES</span></span>

## <span data-ttu-id="a9996-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9996-130">RELATED LINKS</span></span>
