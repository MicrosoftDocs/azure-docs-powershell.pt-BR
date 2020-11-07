---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945489"
---
# <span data-ttu-id="50d97-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="50d97-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="50d97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50d97-102">SYNOPSIS</span></span>
<span data-ttu-id="50d97-103">Remove a rota padrão para tráfego de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="50d97-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="50d97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50d97-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50d97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50d97-105">DESCRIPTION</span></span>
<span data-ttu-id="50d97-106">O cmdlet **Remove-AzureVNetGatewayDefaultSite** remove a rota padrão para o site local para o tráfego de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="50d97-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="50d97-107">Esse cmdlet Remove a rota de um gateway de rede virtual privada (VPN) do Azure para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="50d97-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="50d97-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50d97-108">EXAMPLES</span></span>

### <span data-ttu-id="50d97-109">Exemplo 1: remover uma rota para o site padrão</span><span class="sxs-lookup"><span data-stu-id="50d97-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="50d97-110">Esse comando Remove a rota para o site padrão da VPN da rede virtual chamada ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="50d97-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="50d97-111">OS</span><span class="sxs-lookup"><span data-stu-id="50d97-111">PARAMETERS</span></span>

### <span data-ttu-id="50d97-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="50d97-112">-Profile</span></span>
<span data-ttu-id="50d97-113">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="50d97-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50d97-114">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="50d97-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50d97-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="50d97-115">-VNetName</span></span>
<span data-ttu-id="50d97-116">Especifica uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="50d97-116">Specifies a virtual network.</span></span>
<span data-ttu-id="50d97-117">Esse cmdlet Remove a rota padrão do gateway VPN para a rede virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="50d97-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="50d97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d97-118">CommonParameters</span></span>
<span data-ttu-id="50d97-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d97-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d97-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d97-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50d97-121">INPUTS</span></span>

## <span data-ttu-id="50d97-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50d97-122">OUTPUTS</span></span>

## <span data-ttu-id="50d97-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50d97-123">NOTES</span></span>

## <span data-ttu-id="50d97-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50d97-124">RELATED LINKS</span></span>

[<span data-ttu-id="50d97-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="50d97-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
