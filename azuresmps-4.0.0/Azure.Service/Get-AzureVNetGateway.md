---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946279"
---
# <span data-ttu-id="dc0cc-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="dc0cc-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="dc0cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0cc-103">Obtém o status de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="dc0cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc0cc-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc0cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0cc-106">O cmdlet **Get-AzureVNetGateway** Obtém o status de um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="dc0cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="dc0cc-108">Exemplo 1: obter o status de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dc0cc-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="dc0cc-109">Esse comando obtém o status do gateway de rede virtual para a rede virtual chamada ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="dc0cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc0cc-110">PARAMETERS</span></span>

### <span data-ttu-id="dc0cc-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dc0cc-111">-Profile</span></span>
<span data-ttu-id="dc0cc-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dc0cc-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc0cc-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="dc0cc-114">-VNetName</span></span>
<span data-ttu-id="dc0cc-115">Especifica a rede virtual que contém o gateway de rede virtual para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="dc0cc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0cc-116">CommonParameters</span></span>
<span data-ttu-id="dc0cc-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0cc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0cc-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc0cc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0cc-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc0cc-119">INPUTS</span></span>

## <span data-ttu-id="dc0cc-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc0cc-120">OUTPUTS</span></span>

## <span data-ttu-id="dc0cc-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc0cc-121">NOTES</span></span>

## <span data-ttu-id="dc0cc-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc0cc-122">RELATED LINKS</span></span>

[<span data-ttu-id="dc0cc-123">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="dc0cc-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="dc0cc-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="dc0cc-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="dc0cc-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="dc0cc-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="dc0cc-126">Redimensionar-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="dc0cc-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="dc0cc-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="dc0cc-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


