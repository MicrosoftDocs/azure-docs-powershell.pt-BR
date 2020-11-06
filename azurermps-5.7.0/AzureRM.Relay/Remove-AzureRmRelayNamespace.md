---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428814"
---
# <span data-ttu-id="c1a4b-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c1a4b-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="c1a4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a4b-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1a4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1a4b-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a4b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a4b-106">O cmdlet **Remove-AzureRmRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="c1a4b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1a4b-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a4b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1a4b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="c1a4b-109">Remove o namespace de retransmissão `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="c1a4b-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="c1a4b-110">OS</span><span class="sxs-lookup"><span data-stu-id="c1a4b-110">PARAMETERS</span></span>

### <span data-ttu-id="c1a4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a4b-111">-DefaultProfile</span></span>
<span data-ttu-id="c1a4b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1a4b-113">-Name</span></span>
<span data-ttu-id="c1a4b-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a4b-115">-ResourceGroupName</span></span>
<span data-ttu-id="c1a4b-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1a4b-117">-Confirm</span></span>
<span data-ttu-id="c1a4b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a4b-119">-WhatIf</span></span>
<span data-ttu-id="c1a4b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a4b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a4b-122">CommonParameters</span></span>
<span data-ttu-id="c1a4b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a4b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a4b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a4b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1a4b-125">INPUTS</span></span>

### <span data-ttu-id="c1a4b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a4b-126">-ResourceGroupName</span></span>
 <span data-ttu-id="c1a4b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c1a4b-127">System.String</span></span>

### <span data-ttu-id="c1a4b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1a4b-128">-Name</span></span>
 <span data-ttu-id="c1a4b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c1a4b-129">System.String</span></span>

## <span data-ttu-id="c1a4b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1a4b-130">OUTPUTS</span></span>

### <span data-ttu-id="c1a4b-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="c1a4b-131">System.Object</span></span>

## <span data-ttu-id="c1a4b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1a4b-132">NOTES</span></span>

## <span data-ttu-id="c1a4b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1a4b-133">RELATED LINKS</span></span>

