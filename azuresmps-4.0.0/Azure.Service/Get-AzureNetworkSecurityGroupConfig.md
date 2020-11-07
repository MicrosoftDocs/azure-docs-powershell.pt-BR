---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946333"
---
# <span data-ttu-id="b0121-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="b0121-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="b0121-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0121-102">SYNOPSIS</span></span>
<span data-ttu-id="b0121-103">Obtém detalhes de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b0121-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="b0121-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0121-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0121-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0121-105">DESCRIPTION</span></span>
<span data-ttu-id="b0121-106">O cmdlet **Get-AzureNetworkSecurityGroupConfig** retorna detalhes de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b0121-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="b0121-107">Especifique o parâmetro *detalhado* para exibir as regras de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b0121-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="b0121-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0121-108">EXAMPLES</span></span>

## <span data-ttu-id="b0121-109">OS</span><span class="sxs-lookup"><span data-stu-id="b0121-109">PARAMETERS</span></span>

### <span data-ttu-id="b0121-110">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="b0121-110">-Detailed</span></span>
<span data-ttu-id="b0121-111">Indica que esse cmdlet exibe as regras de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b0121-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="b0121-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b0121-112">-Profile</span></span>
<span data-ttu-id="b0121-113">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b0121-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b0121-114">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b0121-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0121-115">-VM</span><span class="sxs-lookup"><span data-stu-id="b0121-115">-VM</span></span>
<span data-ttu-id="b0121-116">Especifica a máquina virtual para a qual esse cmdlet obtém os detalhes de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b0121-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0121-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0121-117">CommonParameters</span></span>
<span data-ttu-id="b0121-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0121-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0121-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0121-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0121-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0121-120">INPUTS</span></span>

## <span data-ttu-id="b0121-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0121-121">OUTPUTS</span></span>

## <span data-ttu-id="b0121-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0121-122">NOTES</span></span>

## <span data-ttu-id="b0121-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0121-123">RELATED LINKS</span></span>

[<span data-ttu-id="b0121-124">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b0121-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b0121-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b0121-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


