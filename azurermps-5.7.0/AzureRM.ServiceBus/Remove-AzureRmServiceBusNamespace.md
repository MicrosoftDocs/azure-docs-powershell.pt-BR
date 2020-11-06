---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602837"
---
# <span data-ttu-id="f130e-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f130e-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="f130e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f130e-102">SYNOPSIS</span></span>
<span data-ttu-id="f130e-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f130e-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f130e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f130e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f130e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f130e-105">DESCRIPTION</span></span>
<span data-ttu-id="f130e-106">O cmdlet **Remove-AzureRmServiceBusNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f130e-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f130e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f130e-107">EXAMPLES</span></span>

### <span data-ttu-id="f130e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f130e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="f130e-109">Remove o namespace de barramento do serviço `SB-Example1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="f130e-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="f130e-110">OS</span><span class="sxs-lookup"><span data-stu-id="f130e-110">PARAMETERS</span></span>

### <span data-ttu-id="f130e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f130e-111">-DefaultProfile</span></span>
<span data-ttu-id="f130e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f130e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f130e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f130e-113">-Name</span></span>
<span data-ttu-id="f130e-114">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f130e-114">Namespace Name.</span></span>

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

### <span data-ttu-id="f130e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f130e-115">-ResourceGroupName</span></span>
<span data-ttu-id="f130e-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f130e-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f130e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f130e-117">-Confirm</span></span>
<span data-ttu-id="f130e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f130e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f130e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f130e-119">-WhatIf</span></span>
<span data-ttu-id="f130e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f130e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f130e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f130e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f130e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f130e-122">CommonParameters</span></span>
<span data-ttu-id="f130e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f130e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f130e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f130e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f130e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f130e-125">INPUTS</span></span>

### <span data-ttu-id="f130e-126">-Resource</span><span class="sxs-lookup"><span data-stu-id="f130e-126">-ResourceGroup</span></span>
 <span data-ttu-id="f130e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f130e-127">System.String</span></span>

### <span data-ttu-id="f130e-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f130e-128">-NamespaceName</span></span>
 <span data-ttu-id="f130e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f130e-129">System.String</span></span>

## <span data-ttu-id="f130e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f130e-130">OUTPUTS</span></span>

### <span data-ttu-id="f130e-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="f130e-131">System.Object</span></span>

## <span data-ttu-id="f130e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f130e-132">NOTES</span></span>

## <span data-ttu-id="f130e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f130e-133">RELATED LINKS</span></span>

