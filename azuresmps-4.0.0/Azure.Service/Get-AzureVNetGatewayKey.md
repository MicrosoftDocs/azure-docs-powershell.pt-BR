---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946275"
---
# <span data-ttu-id="adcc6-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="adcc6-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="adcc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adcc6-102">SYNOPSIS</span></span>
<span data-ttu-id="adcc6-103">Obtém a chave pré-compartilhada para a conexão entre um gateway de rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="adcc6-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="adcc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adcc6-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="adcc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adcc6-105">DESCRIPTION</span></span>
<span data-ttu-id="adcc6-106">O cmdlet **Get-AzureVNetGatewayKey** Obtém a chave pré-compartilhada para a conexão entre um gateway de rede virtual e um site de rede local.</span><span class="sxs-lookup"><span data-stu-id="adcc6-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="adcc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adcc6-107">EXAMPLES</span></span>

## <span data-ttu-id="adcc6-108">OS</span><span class="sxs-lookup"><span data-stu-id="adcc6-108">PARAMETERS</span></span>

### <span data-ttu-id="adcc6-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="adcc6-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="adcc6-110">Especifica o nome do site de rede local que se conecta ao gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="adcc6-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="adcc6-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="adcc6-111">-Profile</span></span>
<span data-ttu-id="adcc6-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="adcc6-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="adcc6-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="adcc6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="adcc6-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="adcc6-114">-VNetName</span></span>
<span data-ttu-id="adcc6-115">Especifica a rede virtual para a qual esse cmdlet obtém a chave compartilhada para conexões.</span><span class="sxs-lookup"><span data-stu-id="adcc6-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="adcc6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcc6-116">CommonParameters</span></span>
<span data-ttu-id="adcc6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcc6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcc6-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcc6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcc6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adcc6-119">INPUTS</span></span>

## <span data-ttu-id="adcc6-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adcc6-120">OUTPUTS</span></span>

## <span data-ttu-id="adcc6-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adcc6-121">NOTES</span></span>

## <span data-ttu-id="adcc6-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adcc6-122">RELATED LINKS</span></span>

[<span data-ttu-id="adcc6-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="adcc6-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


