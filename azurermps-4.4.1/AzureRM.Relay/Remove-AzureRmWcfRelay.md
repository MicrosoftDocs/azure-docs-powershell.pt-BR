---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440967"
---
# <span data-ttu-id="dd2d2-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd2d2-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="dd2d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd2d2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2d2-103">Remove o WcfRelay do namespace especificado de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd2d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd2d2-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd2d2-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2d2-106">O cmdlet **Remove-AzureRmWcfRelay** remove o WcfRelay do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="dd2d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd2d2-107">EXAMPLES</span></span>

### <span data-ttu-id="dd2d2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd2d2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="dd2d2-109">Remove o WcfRelay `TestWCFRelay1` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="dd2d2-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="dd2d2-110">OS</span><span class="sxs-lookup"><span data-stu-id="dd2d2-110">PARAMETERS</span></span>

### <span data-ttu-id="dd2d2-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd2d2-111">-Namespace</span></span>
<span data-ttu-id="dd2d2-112">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-112">Namespace Name.</span></span>

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

### <span data-ttu-id="dd2d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="dd2d2-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd2d2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd2d2-115">-Name</span></span>
<span data-ttu-id="dd2d2-116">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dd2d2-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd2d2-117">-Confirm</span></span>
<span data-ttu-id="dd2d2-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2d2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2d2-119">-WhatIf</span></span>
<span data-ttu-id="dd2d2-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2d2-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2d2-122">-DefaultProfile</span></span>
<span data-ttu-id="dd2d2-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd2d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2d2-124">CommonParameters</span></span>
<span data-ttu-id="dd2d2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2d2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2d2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2d2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd2d2-127">INPUTS</span></span>

### <span data-ttu-id="dd2d2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2d2-128">-ResourceGroupName</span></span>
 <span data-ttu-id="dd2d2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2d2-129">System.String</span></span>
 

### <span data-ttu-id="dd2d2-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd2d2-130">-Namespace</span></span>
 <span data-ttu-id="dd2d2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2d2-131">System.String</span></span>
 

### <span data-ttu-id="dd2d2-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd2d2-132">-Name</span></span>
 <span data-ttu-id="dd2d2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2d2-133">System.String</span></span>

## <span data-ttu-id="dd2d2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd2d2-134">OUTPUTS</span></span>

### <span data-ttu-id="dd2d2-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="dd2d2-135">System.Object</span></span>

## <span data-ttu-id="dd2d2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd2d2-136">NOTES</span></span>

## <span data-ttu-id="dd2d2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd2d2-137">RELATED LINKS</span></span>

