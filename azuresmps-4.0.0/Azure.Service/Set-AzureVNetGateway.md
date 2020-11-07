---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946414"
---
# <span data-ttu-id="d3c39-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="d3c39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3c39-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c39-103">Habilita ou desabilita um gateway VPN para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c39-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="d3c39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3c39-104">SYNTAX</span></span>

### <span data-ttu-id="d3c39-105">Conectar (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3c39-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3c39-106">Automática</span><span class="sxs-lookup"><span data-stu-id="d3c39-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3c39-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3c39-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c39-108">O cmdlet **set-AzureVNetGateway** habilita ou desabilita um gateway de rede virtual privada (VPN) para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c39-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="d3c39-109">Um gateway de rede virtual é um ponto de extremidade VPN para se conectar a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d3c39-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="d3c39-110">Especifique o parâmetro *Connect* ou *Disconnect* para habilitar ou desabilitar a conexão VPN entre um site de rede local e uma rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="d3c39-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="d3c39-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3c39-111">EXAMPLES</span></span>

### <span data-ttu-id="d3c39-112">Exemplo 1: habilitar um gateway de rede virtual para uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="d3c39-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="d3c39-113">Esse comando habilita o gateway de rede virtual entre a rede virtual do Azure nomeada ContosoProdNet e o dispositivo VPN para o site de rede local chamado ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="d3c39-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="d3c39-114">Exemplo 2: desabilitar um gateway de rede virtual para uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="d3c39-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="d3c39-115">Esse comando desabilita o gateway de rede virtual entre a rede virtual do Azure chamada ContosoProdNet e o dispositivo VPN para o site de rede local chamado ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="d3c39-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="d3c39-116">OS</span><span class="sxs-lookup"><span data-stu-id="d3c39-116">PARAMETERS</span></span>

### <span data-ttu-id="d3c39-117">-Conectar</span><span class="sxs-lookup"><span data-stu-id="d3c39-117">-Connect</span></span>
<span data-ttu-id="d3c39-118">Indica que esse cmdlet habilita a conexão VPN entre uma rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="d3c39-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c39-119">-Desconectar</span><span class="sxs-lookup"><span data-stu-id="d3c39-119">-Disconnect</span></span>
<span data-ttu-id="d3c39-120">Indica que esse cmdlet desabilita a conexão VPN entre uma rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="d3c39-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c39-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d3c39-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d3c39-122">Especifica o nome do site de rede local no local para o qual este cmdlet habilita ou desabilita a conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="d3c39-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c39-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d3c39-123">-Profile</span></span>
<span data-ttu-id="d3c39-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d3c39-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d3c39-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d3c39-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c39-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d3c39-126">-VNetName</span></span>
<span data-ttu-id="d3c39-127">Especifica a rede virtual para a qual esse cmdlet habilita ou desabilita a conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="d3c39-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c39-128">CommonParameters</span></span>
<span data-ttu-id="d3c39-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c39-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c39-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c39-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3c39-131">INPUTS</span></span>

## <span data-ttu-id="d3c39-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3c39-132">OUTPUTS</span></span>

## <span data-ttu-id="d3c39-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3c39-133">NOTES</span></span>

## <span data-ttu-id="d3c39-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3c39-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3c39-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="d3c39-136">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="d3c39-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="d3c39-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="d3c39-139">Redimensionar-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d3c39-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


