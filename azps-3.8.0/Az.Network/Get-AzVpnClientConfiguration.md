---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943544"
---
# <span data-ttu-id="40d49-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d49-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="40d49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40d49-102">SYNOPSIS</span></span>
<span data-ttu-id="40d49-103">Permite que os usuários baixem facilmente o pacote de perfil VPN gerado usando o New-AzVpnClientConfiguration commandlet.</span><span class="sxs-lookup"><span data-stu-id="40d49-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="40d49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40d49-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40d49-105">DESCRIPTION</span></span>
<span data-ttu-id="40d49-106">A Get-AzVpnClientConfiguration retorna a URL da qual o cliente VPN pode ser baixado.</span><span class="sxs-lookup"><span data-stu-id="40d49-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="40d49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40d49-107">EXAMPLES</span></span>

### <span data-ttu-id="40d49-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40d49-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="40d49-109">Obtém a URL para baixar um perfil do VpnClient que foi gerado anteriormente usando o comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="40d49-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="40d49-110">OS</span><span class="sxs-lookup"><span data-stu-id="40d49-110">PARAMETERS</span></span>

### <span data-ttu-id="40d49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d49-111">-DefaultProfile</span></span>
<span data-ttu-id="40d49-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40d49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d49-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="40d49-113">-Name</span></span>
<span data-ttu-id="40d49-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="40d49-114">The resource name.</span></span>

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

### <span data-ttu-id="40d49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d49-115">-ResourceGroupName</span></span>
<span data-ttu-id="40d49-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40d49-116">The resource group name.</span></span>

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

### <span data-ttu-id="40d49-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40d49-117">-Confirm</span></span>
<span data-ttu-id="40d49-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d49-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d49-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d49-119">-WhatIf</span></span>
<span data-ttu-id="40d49-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40d49-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40d49-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40d49-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d49-122">CommonParameters</span></span>
<span data-ttu-id="40d49-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d49-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40d49-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d49-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40d49-125">INPUTS</span></span>

### <span data-ttu-id="40d49-126">System. String</span><span class="sxs-lookup"><span data-stu-id="40d49-126">System.String</span></span>

## <span data-ttu-id="40d49-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40d49-127">OUTPUTS</span></span>

### <span data-ttu-id="40d49-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="40d49-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="40d49-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40d49-129">NOTES</span></span>

## <span data-ttu-id="40d49-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40d49-130">RELATED LINKS</span></span>

[<span data-ttu-id="40d49-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d49-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
