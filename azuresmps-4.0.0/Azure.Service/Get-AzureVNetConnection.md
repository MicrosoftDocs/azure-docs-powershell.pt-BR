---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946287"
---
# <span data-ttu-id="543e1-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="543e1-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="543e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="543e1-102">SYNOPSIS</span></span>
<span data-ttu-id="543e1-103">Obtém conexões com uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="543e1-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="543e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="543e1-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="543e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="543e1-105">DESCRIPTION</span></span>
<span data-ttu-id="543e1-106">O cmdlet **Get-AzureVNetConnection** retorna um objeto que especifica todas as conexões de rede virtual privada (VPN) ativas para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="543e1-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="543e1-107">As conexões VPN incluem VPNs entre sites e redes locais entre sites e redes virtuais para conexões de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="543e1-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="543e1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="543e1-108">EXAMPLES</span></span>

## <span data-ttu-id="543e1-109">OS</span><span class="sxs-lookup"><span data-stu-id="543e1-109">PARAMETERS</span></span>

### <span data-ttu-id="543e1-110">-Perfil</span><span class="sxs-lookup"><span data-stu-id="543e1-110">-Profile</span></span>
<span data-ttu-id="543e1-111">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="543e1-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="543e1-112">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="543e1-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="543e1-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="543e1-113">-VNetName</span></span>
<span data-ttu-id="543e1-114">Especifica o nome da rede virtual a partir da qual esse cmdlet retorna conexões.</span><span class="sxs-lookup"><span data-stu-id="543e1-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="543e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="543e1-115">CommonParameters</span></span>
<span data-ttu-id="543e1-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="543e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="543e1-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="543e1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="543e1-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="543e1-118">INPUTS</span></span>

## <span data-ttu-id="543e1-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="543e1-119">OUTPUTS</span></span>

## <span data-ttu-id="543e1-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="543e1-120">NOTES</span></span>

## <span data-ttu-id="543e1-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="543e1-121">RELATED LINKS</span></span>

