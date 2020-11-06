---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441344"
---
# <span data-ttu-id="fb5a8-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="fb5a8-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="fb5a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5a8-103">Remove o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb5a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb5a8-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb5a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb5a8-105">DESCRIPTION</span></span>
<span data-ttu-id="fb5a8-106">O cmdlet Remove-AzureRmEventHub remove e exclui o Hub de eventos especificado do namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="fb5a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb5a8-107">EXAMPLES</span></span>

### <span data-ttu-id="fb5a8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb5a8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="fb5a8-109">Remove o Hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="fb5a8-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="fb5a8-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb5a8-110">PARAMETERS</span></span>

### <span data-ttu-id="fb5a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5a8-111">-DefaultProfile</span></span>
<span data-ttu-id="fb5a8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb5a8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb5a8-113">-Name</span></span>
<span data-ttu-id="fb5a8-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="fb5a8-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb5a8-115">-Namespace</span></span>
<span data-ttu-id="fb5a8-116">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="fb5a8-116">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb5a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb5a8-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fb5a8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fb5a8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb5a8-119">-Confirm</span></span>
<span data-ttu-id="fb5a8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb5a8-121">-WhatIf</span></span>
<span data-ttu-id="fb5a8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb5a8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5a8-124">CommonParameters</span></span>
<span data-ttu-id="fb5a8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fb5a8-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb5a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5a8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb5a8-127">INPUTS</span></span>

### <span data-ttu-id="fb5a8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb5a8-128">System.String</span></span>


## <span data-ttu-id="fb5a8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb5a8-129">OUTPUTS</span></span>

### <span data-ttu-id="fb5a8-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="fb5a8-130">System.Object</span></span>

## <span data-ttu-id="fb5a8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb5a8-131">NOTES</span></span>

## <span data-ttu-id="fb5a8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb5a8-132">RELATED LINKS</span></span>
