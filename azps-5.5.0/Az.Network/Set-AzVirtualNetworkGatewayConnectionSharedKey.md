---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111547"
---
# <span data-ttu-id="aa572-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aa572-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="aa572-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa572-102">SYNOPSIS</span></span>
<span data-ttu-id="aa572-103">Configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa572-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="aa572-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa572-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa572-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa572-105">DESCRIPTION</span></span>
<span data-ttu-id="aa572-106">O cmdlet **Set-AzVirtualNetworkGatewayConnectionSharedKey** configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa572-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="aa572-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa572-107">EXAMPLES</span></span>

### <span data-ttu-id="aa572-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa572-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="aa572-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa572-109">PARAMETERS</span></span>

### <span data-ttu-id="aa572-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa572-110">-DefaultProfile</span></span>
<span data-ttu-id="aa572-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aa572-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa572-112">-Forçar</span><span class="sxs-lookup"><span data-stu-id="aa572-112">-Force</span></span>
<span data-ttu-id="aa572-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa572-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa572-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa572-114">-Name</span></span>
<span data-ttu-id="aa572-115">Especifica o nome da chave compartilhada do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa572-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="aa572-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa572-116">-ResourceGroupName</span></span>
<span data-ttu-id="aa572-117">Especifica o nome do grupo de recursos a que o gateway de rede virtual pertence</span><span class="sxs-lookup"><span data-stu-id="aa572-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="aa572-118">-Valor</span><span class="sxs-lookup"><span data-stu-id="aa572-118">-Value</span></span>
<span data-ttu-id="aa572-119">Especifica o valor da chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="aa572-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="aa572-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aa572-120">-Confirm</span></span>
<span data-ttu-id="aa572-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa572-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa572-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa572-122">-WhatIf</span></span>
<span data-ttu-id="aa572-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aa572-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa572-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa572-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa572-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa572-125">CommonParameters</span></span>
<span data-ttu-id="aa572-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa572-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa572-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa572-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa572-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="aa572-128">INPUTS</span></span>

### <span data-ttu-id="aa572-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aa572-129">System.String</span></span>

## <span data-ttu-id="aa572-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="aa572-130">OUTPUTS</span></span>

### <span data-ttu-id="aa572-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aa572-131">System.String</span></span>

## <span data-ttu-id="aa572-132">Notas</span><span class="sxs-lookup"><span data-stu-id="aa572-132">NOTES</span></span>

## <span data-ttu-id="aa572-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa572-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa572-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aa572-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="aa572-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aa572-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
