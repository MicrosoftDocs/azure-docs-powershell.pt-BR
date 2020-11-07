---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945465"
---
# <span data-ttu-id="997b1-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="997b1-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="997b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="997b1-102">SYNOPSIS</span></span>
<span data-ttu-id="997b1-103">Redefine um gateway VPN de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="997b1-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="997b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="997b1-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="997b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="997b1-105">DESCRIPTION</span></span>
<span data-ttu-id="997b1-106">O cmdlet **Reset-AzureVNetGateway** redefine e reinicia um gateway de rede virtual de rede privada virtual (VPN).</span><span class="sxs-lookup"><span data-stu-id="997b1-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="997b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="997b1-107">EXAMPLES</span></span>

### <span data-ttu-id="997b1-108">Exemplo 1: redefinir um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="997b1-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="997b1-109">Esse comando redefine o gateway de rede virtual da rede virtual chamada ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="997b1-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="997b1-110">OS</span><span class="sxs-lookup"><span data-stu-id="997b1-110">PARAMETERS</span></span>

### <span data-ttu-id="997b1-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="997b1-111">-Profile</span></span>
<span data-ttu-id="997b1-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="997b1-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="997b1-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="997b1-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="997b1-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="997b1-114">-VNetName</span></span>
<span data-ttu-id="997b1-115">Especifica a rede virtual que contém o gateway de rede virtual que este cmdlet redefine.</span><span class="sxs-lookup"><span data-stu-id="997b1-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="997b1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997b1-116">CommonParameters</span></span>
<span data-ttu-id="997b1-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="997b1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997b1-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="997b1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997b1-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="997b1-119">INPUTS</span></span>

## <span data-ttu-id="997b1-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="997b1-120">OUTPUTS</span></span>

## <span data-ttu-id="997b1-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="997b1-121">NOTES</span></span>

## <span data-ttu-id="997b1-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="997b1-122">RELATED LINKS</span></span>

[<span data-ttu-id="997b1-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="997b1-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="997b1-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="997b1-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="997b1-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="997b1-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="997b1-126">Redimensionar-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="997b1-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="997b1-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="997b1-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


