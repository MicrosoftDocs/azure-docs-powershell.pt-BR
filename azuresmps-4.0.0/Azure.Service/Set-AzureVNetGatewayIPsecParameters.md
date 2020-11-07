---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946036"
---
# <span data-ttu-id="6f330-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="6f330-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="6f330-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f330-102">SYNOPSIS</span></span>
<span data-ttu-id="6f330-103">Define os parâmetros IPsec para a conexão entre um gateway de rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="6f330-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="6f330-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f330-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f330-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f330-105">DESCRIPTION</span></span>
<span data-ttu-id="6f330-106">O cmdlet **set-AzureVNetGatewayIPsecParameters** define a segurança do protocolo Internet (IPSec) e os parâmetros de troca de chaves na Internet (IKE) para a conexão entre um gateway de rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="6f330-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="6f330-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f330-107">EXAMPLES</span></span>

## <span data-ttu-id="6f330-108">OS</span><span class="sxs-lookup"><span data-stu-id="6f330-108">PARAMETERS</span></span>

### <span data-ttu-id="6f330-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="6f330-109">-EncryptionType</span></span>
<span data-ttu-id="6f330-110">Especifica o tipo de criptografia do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6f330-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="6f330-111">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6f330-111">Valid values are:</span></span> 

- <span data-ttu-id="6f330-112">Descriptografia</span><span class="sxs-lookup"><span data-stu-id="6f330-112">NoEncryption</span></span> 
- <span data-ttu-id="6f330-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="6f330-113">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f330-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="6f330-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="6f330-115">Especifica o nome da conexão do site de rede local em que esse cmdlet configura os parâmetros IPsec e IKE.</span><span class="sxs-lookup"><span data-stu-id="6f330-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="6f330-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6f330-116">-PfsGroup</span></span>
<span data-ttu-id="6f330-117">Especifica o grupo sigilo total na transferência (PFS).</span><span class="sxs-lookup"><span data-stu-id="6f330-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="6f330-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6f330-118">Valid values are:</span></span> 

- <span data-ttu-id="6f330-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="6f330-119">PFS1</span></span> 
- <span data-ttu-id="6f330-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f330-120">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f330-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6f330-121">-Profile</span></span>
<span data-ttu-id="6f330-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6f330-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6f330-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6f330-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f330-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="6f330-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="6f330-125">Especifica o tamanho, em kilobytes, da Associação de segurança (SA).</span><span class="sxs-lookup"><span data-stu-id="6f330-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f330-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="6f330-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="6f330-127">Especifica o período, em segundos, da Associação de segurança.</span><span class="sxs-lookup"><span data-stu-id="6f330-127">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f330-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="6f330-128">-VNetName</span></span>
<span data-ttu-id="6f330-129">Especifica a rede virtual para a qual esse cmdlet define os parâmetros IPsec para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6f330-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="6f330-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f330-130">CommonParameters</span></span>
<span data-ttu-id="6f330-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f330-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f330-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f330-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f330-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f330-133">INPUTS</span></span>

## <span data-ttu-id="6f330-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f330-134">OUTPUTS</span></span>

## <span data-ttu-id="6f330-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f330-135">NOTES</span></span>

## <span data-ttu-id="6f330-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f330-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f330-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="6f330-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


