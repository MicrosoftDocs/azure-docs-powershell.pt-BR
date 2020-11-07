---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946570"
---
# <span data-ttu-id="decde-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="decde-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="decde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="decde-102">SYNOPSIS</span></span>
<span data-ttu-id="decde-103">Recupera informações sobre as redes virtuais do Azure RemoteApp no Azure.</span><span class="sxs-lookup"><span data-stu-id="decde-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="decde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="decde-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="decde-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="decde-105">DESCRIPTION</span></span>
<span data-ttu-id="decde-106">O cmdlet **Get-AzureRemoteAppVNet** recupera informações sobre as redes virtuais do Azure RemoteApp no Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="decde-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="decde-107">Esse cmdlet retorna um objeto que contém informações sobre uma rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="decde-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="decde-108">Se nenhuma rede virtual for especificada, esse cmdlet retornará informações sobre todas as redes virtuais na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="decde-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="decde-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="decde-109">EXAMPLES</span></span>

### <span data-ttu-id="decde-110">Exemplo 1: recuperar informações sobre uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="decde-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="decde-111">Esse comando obtém informações sobre a rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="decde-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="decde-112">OS</span><span class="sxs-lookup"><span data-stu-id="decde-112">PARAMETERS</span></span>

### <span data-ttu-id="decde-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="decde-113">-IncludeSharedKey</span></span>
<span data-ttu-id="decde-114">Indica que esse cmdlet inclui o valor da chave compartilhada nas informações que ele recupera sobre a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="decde-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decde-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="decde-115">-Profile</span></span>
<span data-ttu-id="decde-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="decde-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="decde-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="decde-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="decde-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="decde-118">-VNetName</span></span>
<span data-ttu-id="decde-119">Especifica o nome da rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="decde-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="decde-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decde-120">CommonParameters</span></span>
<span data-ttu-id="decde-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decde-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decde-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="decde-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decde-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="decde-123">INPUTS</span></span>

## <span data-ttu-id="decde-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="decde-124">OUTPUTS</span></span>

## <span data-ttu-id="decde-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="decde-125">NOTES</span></span>

## <span data-ttu-id="decde-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="decde-126">RELATED LINKS</span></span>

[<span data-ttu-id="decde-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="decde-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


