---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775465"
---
# <span data-ttu-id="d71bf-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d71bf-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="d71bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d71bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d71bf-103">Permite que os usuários baixem facilmente o pacote de perfil VPN gerado usando o New-AzVpnClientConfiguration commandlet.</span><span class="sxs-lookup"><span data-stu-id="d71bf-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="d71bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d71bf-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d71bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d71bf-105">DESCRIPTION</span></span>
<span data-ttu-id="d71bf-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="d71bf-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d71bf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d71bf-107">EXAMPLES</span></span>

### <span data-ttu-id="d71bf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d71bf-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="d71bf-109">Obtém a URL para baixar um perfil do VpnClient que foi gerado anteriormente usando o comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d71bf-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="d71bf-110">OS</span><span class="sxs-lookup"><span data-stu-id="d71bf-110">PARAMETERS</span></span>

### <span data-ttu-id="d71bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71bf-111">-DefaultProfile</span></span>
<span data-ttu-id="d71bf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d71bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="d71bf-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d71bf-113">-Name</span></span>
<span data-ttu-id="d71bf-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d71bf-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d71bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="d71bf-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d71bf-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71bf-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d71bf-117">-Confirm</span></span>
<span data-ttu-id="d71bf-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d71bf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d71bf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d71bf-119">-WhatIf</span></span>
<span data-ttu-id="d71bf-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d71bf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d71bf-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d71bf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d71bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71bf-122">CommonParameters</span></span>
<span data-ttu-id="d71bf-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71bf-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d71bf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71bf-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d71bf-125">INPUTS</span></span>

### <span data-ttu-id="d71bf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d71bf-126">System.String</span></span>

## <span data-ttu-id="d71bf-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d71bf-127">OUTPUTS</span></span>

### <span data-ttu-id="d71bf-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="d71bf-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="d71bf-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d71bf-129">NOTES</span></span>

## <span data-ttu-id="d71bf-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d71bf-130">RELATED LINKS</span></span>
