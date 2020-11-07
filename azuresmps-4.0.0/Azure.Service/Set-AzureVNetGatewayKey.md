---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945810"
---
# <span data-ttu-id="dfafb-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="dfafb-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="dfafb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfafb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfafb-103">Define a chave pré-compartilhada para a conexão entre um gateway de VPN do Azure e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="dfafb-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="dfafb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfafb-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dfafb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfafb-105">DESCRIPTION</span></span>
<span data-ttu-id="dfafb-106">O cmdlet **set-AzureVNetGatewayKey** define a chave pré-compartilhada para a conexão entre um gateway de rede virtual privada (VPN) do Azure e um site de rede local no local.</span><span class="sxs-lookup"><span data-stu-id="dfafb-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="dfafb-107">A chave deve ser igual à chave configurada no gateway do site de rede local.</span><span class="sxs-lookup"><span data-stu-id="dfafb-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="dfafb-108">Se as chaves não corresponderem, não será possível estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="dfafb-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="dfafb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfafb-109">EXAMPLES</span></span>

## <span data-ttu-id="dfafb-110">OS</span><span class="sxs-lookup"><span data-stu-id="dfafb-110">PARAMETERS</span></span>

### <span data-ttu-id="dfafb-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="dfafb-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="dfafb-112">Especifica o nome do site de rede local que se conecta ao gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dfafb-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="dfafb-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dfafb-113">-Profile</span></span>
<span data-ttu-id="dfafb-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dfafb-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dfafb-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dfafb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dfafb-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="dfafb-116">-SharedKey</span></span>
<span data-ttu-id="dfafb-117">Especifica a chave compartilhada a ser atribuída ao gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="dfafb-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="dfafb-118">O valor deve ser uma cadeia de caracteres alfanuméricos de mais de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dfafb-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="dfafb-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="dfafb-119">-VNetName</span></span>
<span data-ttu-id="dfafb-120">Especifica a rede virtual para a qual esse cmdlet define a chave compartilhada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="dfafb-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="dfafb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfafb-121">CommonParameters</span></span>
<span data-ttu-id="dfafb-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfafb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfafb-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfafb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfafb-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfafb-124">INPUTS</span></span>

## <span data-ttu-id="dfafb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfafb-125">OUTPUTS</span></span>

## <span data-ttu-id="dfafb-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfafb-126">NOTES</span></span>

## <span data-ttu-id="dfafb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfafb-127">RELATED LINKS</span></span>

[<span data-ttu-id="dfafb-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="dfafb-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


