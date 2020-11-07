---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946413"
---
# <span data-ttu-id="a760a-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a760a-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="a760a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a760a-102">SYNOPSIS</span></span>
<span data-ttu-id="a760a-103">Define o site padrão do tráfego de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="a760a-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="a760a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a760a-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a760a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a760a-105">DESCRIPTION</span></span>
<span data-ttu-id="a760a-106">O cmdlet **set-AzureVNetGatewayDefaultSite** define a rota padrão para o site local para o tráfego de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="a760a-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="a760a-107">Esse comando define a rota em um gateway de rede virtual privada (VPN) do Azure para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a760a-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="a760a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a760a-108">EXAMPLES</span></span>

## <span data-ttu-id="a760a-109">OS</span><span class="sxs-lookup"><span data-stu-id="a760a-109">PARAMETERS</span></span>

### <span data-ttu-id="a760a-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="a760a-110">-DefaultSite</span></span>
<span data-ttu-id="a760a-111">Especifica o nome do site de rede local no local para o tráfego de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="a760a-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="a760a-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a760a-112">-Profile</span></span>
<span data-ttu-id="a760a-113">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a760a-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a760a-114">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a760a-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a760a-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a760a-115">-VNetName</span></span>
<span data-ttu-id="a760a-116">Especifica uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a760a-116">Specifies a virtual network.</span></span>
<span data-ttu-id="a760a-117">Este cmdlet define a rota padrão do gateway VPN para o tráfego de encapsulamento forçado para a rede virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a760a-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="a760a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a760a-118">CommonParameters</span></span>
<span data-ttu-id="a760a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a760a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a760a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a760a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a760a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a760a-121">INPUTS</span></span>

## <span data-ttu-id="a760a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a760a-122">OUTPUTS</span></span>

## <span data-ttu-id="a760a-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a760a-123">NOTES</span></span>

## <span data-ttu-id="a760a-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a760a-124">RELATED LINKS</span></span>

[<span data-ttu-id="a760a-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a760a-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
