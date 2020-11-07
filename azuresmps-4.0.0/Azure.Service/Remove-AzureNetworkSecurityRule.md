---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945869"
---
# <span data-ttu-id="82a1d-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="82a1d-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="82a1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="82a1d-103">Remove uma regra de segurança de rede de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="82a1d-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="82a1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82a1d-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82a1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="82a1d-106">O cmdlet **Remove-AzureNetworkSecurityRule** remove uma regra de segurança de rede do Azure de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="82a1d-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="82a1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82a1d-107">EXAMPLES</span></span>

## <span data-ttu-id="82a1d-108">OS</span><span class="sxs-lookup"><span data-stu-id="82a1d-108">PARAMETERS</span></span>

### <span data-ttu-id="82a1d-109">-Force</span><span class="sxs-lookup"><span data-stu-id="82a1d-109">-Force</span></span>
<span data-ttu-id="82a1d-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="82a1d-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82a1d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="82a1d-111">-Name</span></span>
<span data-ttu-id="82a1d-112">Especifica o nome da regra de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="82a1d-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a1d-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82a1d-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="82a1d-114">Especifica o grupo de segurança de rede que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="82a1d-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="82a1d-115">Para obter um objeto **INetworkSecurityGroup** , use o cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="82a1d-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82a1d-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="82a1d-116">-Profile</span></span>
<span data-ttu-id="82a1d-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="82a1d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="82a1d-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="82a1d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82a1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a1d-119">CommonParameters</span></span>
<span data-ttu-id="82a1d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a1d-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a1d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a1d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82a1d-122">INPUTS</span></span>

## <span data-ttu-id="82a1d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82a1d-123">OUTPUTS</span></span>

## <span data-ttu-id="82a1d-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82a1d-124">NOTES</span></span>

## <span data-ttu-id="82a1d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82a1d-125">RELATED LINKS</span></span>

[<span data-ttu-id="82a1d-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="82a1d-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


