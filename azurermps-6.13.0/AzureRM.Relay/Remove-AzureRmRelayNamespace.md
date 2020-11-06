---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: ac6327176c587bcb221a5ebddbb12ae9adeffbf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610253"
---
# <span data-ttu-id="5ce37-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="5ce37-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="5ce37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ce37-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce37-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="5ce37-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ce37-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ce37-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce37-106">O cmdlet **Remove-AzureRmRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="5ce37-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="5ce37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ce37-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce37-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ce37-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="5ce37-109">Remove o namespace de retransmissão `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="5ce37-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="5ce37-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ce37-110">PARAMETERS</span></span>

### <span data-ttu-id="5ce37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce37-111">-DefaultProfile</span></span>
<span data-ttu-id="5ce37-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce37-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce37-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ce37-113">-Name</span></span>
<span data-ttu-id="5ce37-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="5ce37-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="5ce37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce37-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ce37-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ce37-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="5ce37-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ce37-117">-Confirm</span></span>
<span data-ttu-id="5ce37-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce37-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce37-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce37-119">-WhatIf</span></span>
<span data-ttu-id="5ce37-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ce37-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce37-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ce37-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce37-122">CommonParameters</span></span>
<span data-ttu-id="5ce37-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ce37-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce37-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce37-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ce37-125">INPUTS</span></span>

### <span data-ttu-id="5ce37-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce37-126">System.String</span></span>


## <span data-ttu-id="5ce37-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ce37-127">OUTPUTS</span></span>

### <span data-ttu-id="5ce37-128">System. void</span><span class="sxs-lookup"><span data-stu-id="5ce37-128">System.Void</span></span>


## <span data-ttu-id="5ce37-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ce37-129">NOTES</span></span>

## <span data-ttu-id="5ce37-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ce37-130">RELATED LINKS</span></span>
