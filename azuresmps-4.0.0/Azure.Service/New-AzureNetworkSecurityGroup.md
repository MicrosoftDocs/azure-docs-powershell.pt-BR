---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945910"
---
# <span data-ttu-id="d7a91-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7a91-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="d7a91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7a91-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a91-103">Cria um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a91-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="d7a91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7a91-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7a91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7a91-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a91-106">O cmdlet **New-AzureNetworkSecurityGroup** cria um grupo de segurança de rede do Azure em um local.</span><span class="sxs-lookup"><span data-stu-id="d7a91-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="d7a91-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7a91-107">EXAMPLES</span></span>

## <span data-ttu-id="d7a91-108">OS</span><span class="sxs-lookup"><span data-stu-id="d7a91-108">PARAMETERS</span></span>

### <span data-ttu-id="d7a91-109">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="d7a91-109">-Label</span></span>
<span data-ttu-id="d7a91-110">Especifica uma descrição para o novo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="d7a91-110">Specifies a description for the new network security group.</span></span>

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

### <span data-ttu-id="d7a91-111">-Local</span><span class="sxs-lookup"><span data-stu-id="d7a91-111">-Location</span></span>
<span data-ttu-id="d7a91-112">Especifica o local do Azure no qual esse cmdlet cria um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="d7a91-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="d7a91-113">Para obter locais válidos, use o cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="d7a91-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="d7a91-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7a91-114">-Name</span></span>
<span data-ttu-id="d7a91-115">Especifica um nome para o novo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="d7a91-115">Specifies a name for the new network security group.</span></span>

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

### <span data-ttu-id="d7a91-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d7a91-116">-Profile</span></span>
<span data-ttu-id="d7a91-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d7a91-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d7a91-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d7a91-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7a91-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a91-119">CommonParameters</span></span>
<span data-ttu-id="d7a91-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a91-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a91-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a91-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a91-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7a91-122">INPUTS</span></span>

## <span data-ttu-id="d7a91-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7a91-123">OUTPUTS</span></span>

## <span data-ttu-id="d7a91-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7a91-124">NOTES</span></span>

## <span data-ttu-id="d7a91-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7a91-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7a91-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7a91-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


