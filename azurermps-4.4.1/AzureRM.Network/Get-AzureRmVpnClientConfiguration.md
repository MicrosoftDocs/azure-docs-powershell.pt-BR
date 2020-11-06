---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 7050e348530231d9ecc7fbec443f15238f6a41f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611098"
---
# <span data-ttu-id="5d3f0-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f0-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="5d3f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3f0-103">Permite que os usuários baixem facilmente o pacote de perfil VPN gerado usando o New-AzureRmVpnClientConfiguration commandlet.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d3f0-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d3f0-105">DESCRIPTION</span></span>
<span data-ttu-id="5d3f0-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="5d3f0-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5d3f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d3f0-107">EXAMPLES</span></span>

### <span data-ttu-id="5d3f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d3f0-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5d3f0-109">Obtém a URL para baixar um perfil do VpnClient que foi gerado anteriormente usando o comando New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="5d3f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="5d3f0-110">PARAMETERS</span></span>

### <span data-ttu-id="5d3f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f0-111">-DefaultProfile</span></span>
<span data-ttu-id="5d3f0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="5d3f0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d3f0-113">-Name</span></span>
<span data-ttu-id="5d3f0-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-114">The resource name.</span></span>

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

### <span data-ttu-id="5d3f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="5d3f0-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-116">The resource group name.</span></span>

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

### <span data-ttu-id="5d3f0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d3f0-117">-Confirm</span></span>
<span data-ttu-id="5d3f0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d3f0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3f0-119">-WhatIf</span></span>
<span data-ttu-id="5d3f0-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d3f0-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d3f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3f0-122">CommonParameters</span></span>
<span data-ttu-id="5d3f0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3f0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3f0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d3f0-125">INPUTS</span></span>

### <span data-ttu-id="5d3f0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5d3f0-126">System.String</span></span>

## <span data-ttu-id="5d3f0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d3f0-127">OUTPUTS</span></span>

### <span data-ttu-id="5d3f0-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f0-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="5d3f0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d3f0-129">NOTES</span></span>

## <span data-ttu-id="5d3f0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d3f0-130">RELATED LINKS</span></span>

