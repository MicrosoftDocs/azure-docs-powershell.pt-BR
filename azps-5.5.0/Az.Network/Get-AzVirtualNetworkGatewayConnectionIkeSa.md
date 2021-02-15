---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111668"
---
# <span data-ttu-id="e825d-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="e825d-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="e825d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e825d-102">SYNOPSIS</span></span>
<span data-ttu-id="e825d-103">Obter associações de segurança IKE de uma conexão virtual de gateway de rede</span><span class="sxs-lookup"><span data-stu-id="e825d-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="e825d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e825d-104">SYNTAX</span></span>

### <span data-ttu-id="e825d-105">ByName</span><span class="sxs-lookup"><span data-stu-id="e825d-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e825d-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e825d-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e825d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e825d-108">DESCRIPTION</span></span>
<span data-ttu-id="e825d-109">O cmdlet **Get-AzVirtualNetworkGatewayConnectionConnectionConnectionSa** retorna as Associações de Segurança IKE da sua conexão com base no Nome da Conexão e no Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e825d-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="e825d-110">Se o cmdlet **Get-AzVirtualNetworkGatewayConnection** for emitido sem especificar o parâmetro -Name, a saída não mostrará as Associações de Segurança IKE.</span><span class="sxs-lookup"><span data-stu-id="e825d-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="e825d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e825d-111">EXAMPLES</span></span>

### <span data-ttu-id="e825d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e825d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="e825d-113">Retorna as Associações de Segurança IKE para a Conexão virtual de Gateway de Rede com o nome "meuTunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="e825d-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="e825d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e825d-114">PARAMETERS</span></span>

### <span data-ttu-id="e825d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e825d-115">-AsJob</span></span>
<span data-ttu-id="e825d-116">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e825d-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e825d-117">-DefaultProfile</span></span>
<span data-ttu-id="e825d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e825d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e825d-119">-InputObject</span></span>
<span data-ttu-id="e825d-120">O objeto de conexão do gateway de rede virtual para o qual os SAs IKE precisam ser buscados.</span><span class="sxs-lookup"><span data-stu-id="e825d-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e825d-121">-Name</span></span>
<span data-ttu-id="e825d-122">O nome de conexão do gateway de rede virtual para o qual os SAs IKE precisam ser buscados.</span><span class="sxs-lookup"><span data-stu-id="e825d-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e825d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e825d-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e825d-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e825d-125">-ResourceId</span></span>
<span data-ttu-id="e825d-126">A ID de recurso do Azure da Conexão virtual de Gateway de Rede para a qual SAS IKE precisa ser buscada.</span><span class="sxs-lookup"><span data-stu-id="e825d-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e825d-127">CommonParameters</span></span>
<span data-ttu-id="e825d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e825d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e825d-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e825d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e825d-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="e825d-130">INPUTS</span></span>

### <span data-ttu-id="e825d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e825d-131">System.String</span></span>

## <span data-ttu-id="e825d-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="e825d-132">OUTPUTS</span></span>

### <span data-ttu-id="e825d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="e825d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="e825d-134">Notas</span><span class="sxs-lookup"><span data-stu-id="e825d-134">NOTES</span></span>

## <span data-ttu-id="e825d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e825d-135">RELATED LINKS</span></span>
