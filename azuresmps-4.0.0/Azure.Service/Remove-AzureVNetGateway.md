---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945490"
---
# <span data-ttu-id="1306f-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1306f-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="1306f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1306f-102">SYNOPSIS</span></span>
<span data-ttu-id="1306f-103">Exclui um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="1306f-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="1306f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1306f-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1306f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1306f-105">DESCRIPTION</span></span>
<span data-ttu-id="1306f-106">O cmdlet **Remove-AzureVNetGateway** exclui um gateway de rede virtual privada (VPN) existente para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1306f-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="1306f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1306f-107">EXAMPLES</span></span>

### <span data-ttu-id="1306f-108">Exemplo 1: remover um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1306f-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="1306f-109">Esse comando Remove o gateway de rede virtual da rede virtual chamada ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="1306f-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="1306f-110">OS</span><span class="sxs-lookup"><span data-stu-id="1306f-110">PARAMETERS</span></span>

### <span data-ttu-id="1306f-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1306f-111">-Profile</span></span>
<span data-ttu-id="1306f-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1306f-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1306f-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1306f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1306f-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1306f-114">-VNetName</span></span>
<span data-ttu-id="1306f-115">Especifica a rede virtual na qual esse cmdlet exclui o gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="1306f-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="1306f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1306f-116">CommonParameters</span></span>
<span data-ttu-id="1306f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1306f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1306f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1306f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1306f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1306f-119">INPUTS</span></span>

## <span data-ttu-id="1306f-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1306f-120">OUTPUTS</span></span>

## <span data-ttu-id="1306f-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1306f-121">NOTES</span></span>

## <span data-ttu-id="1306f-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1306f-122">RELATED LINKS</span></span>

[<span data-ttu-id="1306f-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1306f-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="1306f-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1306f-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="1306f-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1306f-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="1306f-126">Redimensionar-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1306f-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="1306f-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="1306f-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


