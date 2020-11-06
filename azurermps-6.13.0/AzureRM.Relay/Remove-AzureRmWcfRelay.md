---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429387"
---
# <span data-ttu-id="b95dd-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b95dd-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="b95dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b95dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b95dd-103">Remove o WcfRelay do namespace especificado de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="b95dd-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b95dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b95dd-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b95dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b95dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b95dd-106">O cmdlet **Remove-AzureRmWcfRelay** remove o WcfRelay do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="b95dd-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="b95dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b95dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b95dd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b95dd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="b95dd-109">Remove o WcfRelay `TestWCFRelay1` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b95dd-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b95dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="b95dd-110">PARAMETERS</span></span>

### <span data-ttu-id="b95dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95dd-111">-DefaultProfile</span></span>
<span data-ttu-id="b95dd-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b95dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b95dd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b95dd-113">-Name</span></span>
<span data-ttu-id="b95dd-114">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b95dd-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b95dd-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b95dd-115">-Namespace</span></span>
<span data-ttu-id="b95dd-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b95dd-116">Namespace Name.</span></span>

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

### <span data-ttu-id="b95dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="b95dd-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b95dd-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b95dd-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b95dd-119">-Confirm</span></span>
<span data-ttu-id="b95dd-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b95dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b95dd-121">-WhatIf</span></span>
<span data-ttu-id="b95dd-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b95dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b95dd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b95dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b95dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95dd-124">CommonParameters</span></span>
<span data-ttu-id="b95dd-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b95dd-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95dd-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b95dd-127">INPUTS</span></span>

### <span data-ttu-id="b95dd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b95dd-128">System.String</span></span>


## <span data-ttu-id="b95dd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b95dd-129">OUTPUTS</span></span>

### <span data-ttu-id="b95dd-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b95dd-130">System.Void</span></span>


## <span data-ttu-id="b95dd-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b95dd-131">NOTES</span></span>

## <span data-ttu-id="b95dd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b95dd-132">RELATED LINKS</span></span>