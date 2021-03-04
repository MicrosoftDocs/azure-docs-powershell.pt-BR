---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 03ed4fe9ad6e8b2e7c5af0b24e29c351a2b776f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892955"
---
# <span data-ttu-id="e4ed9-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4ed9-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="e4ed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ed9-103">Permite que os usuários baixem facilmente o pacote de Perfil de Vpn que foi gerado usando o New-AzVpnClientConfiguration commandlet.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="e4ed9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4ed9-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ed9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ed9-106">O Get-AzVpnClientConfiguration retorna a URL da qual o cliente VPN pode ser baixado.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="e4ed9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ed9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4ed9-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e4ed9-109">Obtém a URL para baixar um perfil VpnClient que foi gerado anteriormente usando o comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="e4ed9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-110">PARAMETERS</span></span>

### <span data-ttu-id="e4ed9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ed9-111">-DefaultProfile</span></span>
<span data-ttu-id="e4ed9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ed9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e4ed9-113">-Name</span></span>
<span data-ttu-id="e4ed9-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ed9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4ed9-115">-ResourceGroupName</span></span>
<span data-ttu-id="e4ed9-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-116">The resource group name.</span></span>

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

### <span data-ttu-id="e4ed9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4ed9-117">-Confirm</span></span>
<span data-ttu-id="e4ed9-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ed9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ed9-119">-WhatIf</span></span>
<span data-ttu-id="e4ed9-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4ed9-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4ed9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ed9-122">CommonParameters</span></span>
<span data-ttu-id="e4ed9-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ed9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ed9-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4ed9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ed9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-125">INPUTS</span></span>

### <span data-ttu-id="e4ed9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e4ed9-126">System.String</span></span>

## <span data-ttu-id="e4ed9-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-127">OUTPUTS</span></span>

### <span data-ttu-id="e4ed9-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e4ed9-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e4ed9-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4ed9-129">NOTES</span></span>

## <span data-ttu-id="e4ed9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4ed9-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4ed9-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4ed9-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
