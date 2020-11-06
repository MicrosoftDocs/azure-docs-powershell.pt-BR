---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430717"
---
# <span data-ttu-id="38139-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="38139-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="38139-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38139-102">SYNOPSIS</span></span>
<span data-ttu-id="38139-103">Configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="38139-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38139-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38139-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38139-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38139-105">DESCRIPTION</span></span>
<span data-ttu-id="38139-106">O cmdlet **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="38139-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="38139-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38139-107">EXAMPLES</span></span>

## <span data-ttu-id="38139-108">OS</span><span class="sxs-lookup"><span data-stu-id="38139-108">PARAMETERS</span></span>

### <span data-ttu-id="38139-109">-Force</span><span class="sxs-lookup"><span data-stu-id="38139-109">-Force</span></span>
<span data-ttu-id="38139-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="38139-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38139-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="38139-111">-Name</span></span>
<span data-ttu-id="38139-112">Especifica o nome da chave compartilhada do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="38139-112">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38139-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38139-113">-ResourceGroupName</span></span>
<span data-ttu-id="38139-114">Especifica o nome do grupo de recursos ao qual pertence o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="38139-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38139-115">-Valor</span><span class="sxs-lookup"><span data-stu-id="38139-115">-Value</span></span>
<span data-ttu-id="38139-116">Especifica o valor da chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="38139-116">Specifies the value of the shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38139-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38139-117">-Confirm</span></span>
<span data-ttu-id="38139-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38139-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38139-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38139-119">-WhatIf</span></span>
<span data-ttu-id="38139-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38139-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38139-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38139-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38139-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38139-122">-DefaultProfile</span></span>
<span data-ttu-id="38139-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38139-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38139-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38139-124">CommonParameters</span></span>
<span data-ttu-id="38139-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38139-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38139-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38139-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38139-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38139-127">INPUTS</span></span>

## <span data-ttu-id="38139-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38139-128">OUTPUTS</span></span>

### <span data-ttu-id="38139-129">System. String</span><span class="sxs-lookup"><span data-stu-id="38139-129">System.String</span></span>

## <span data-ttu-id="38139-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38139-130">NOTES</span></span>

## <span data-ttu-id="38139-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38139-131">RELATED LINKS</span></span>

[<span data-ttu-id="38139-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="38139-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="38139-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="38139-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


