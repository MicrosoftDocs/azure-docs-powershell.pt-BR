---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946334"
---
# <span data-ttu-id="54e8c-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54e8c-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="54e8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="54e8c-103">Obtém detalhes de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="54e8c-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="54e8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e8c-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54e8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="54e8c-106">O cmdlet **Get-AzureNetworkSecurityGroup** retorna detalhes de um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="54e8c-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="54e8c-107">Especifique o parâmetro *detalhado* para exibir as regras de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="54e8c-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="54e8c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54e8c-108">EXAMPLES</span></span>

## <span data-ttu-id="54e8c-109">OS</span><span class="sxs-lookup"><span data-stu-id="54e8c-109">PARAMETERS</span></span>

### <span data-ttu-id="54e8c-110">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="54e8c-110">-Detailed</span></span>
<span data-ttu-id="54e8c-111">Indica que esse cmdlet retorna as regras de segurança de rede para o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="54e8c-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="54e8c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="54e8c-112">-Name</span></span>
<span data-ttu-id="54e8c-113">Especifica o nome do grupo de segurança de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="54e8c-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="54e8c-114">Quando um grupo de segurança de rede clássico é criado em um grupo de recursos diferente da ***rede padrão*** usando o portal do Azure, você deve usar a seguinte sintaxe do PowerShell: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="54e8c-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

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

### <span data-ttu-id="54e8c-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="54e8c-115">-Profile</span></span>
<span data-ttu-id="54e8c-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="54e8c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54e8c-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="54e8c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54e8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e8c-118">CommonParameters</span></span>
<span data-ttu-id="54e8c-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e8c-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e8c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e8c-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54e8c-121">INPUTS</span></span>

## <span data-ttu-id="54e8c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54e8c-122">OUTPUTS</span></span>

## <span data-ttu-id="54e8c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54e8c-123">NOTES</span></span>

## <span data-ttu-id="54e8c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54e8c-124">RELATED LINKS</span></span>

[<span data-ttu-id="54e8c-125">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54e8c-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="54e8c-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54e8c-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

