---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775523"
---
# <span data-ttu-id="ccab1-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ccab1-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="ccab1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccab1-102">SYNOPSIS</span></span>
<span data-ttu-id="ccab1-103">Obtém um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ccab1-103">Gets a network security group.</span></span>

## <span data-ttu-id="ccab1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccab1-104">SYNTAX</span></span>

### <span data-ttu-id="ccab1-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="ccab1-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccab1-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="ccab1-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccab1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccab1-107">DESCRIPTION</span></span>
<span data-ttu-id="ccab1-108">O cmdlet **Get-AzNetworkSecurityGroup** Obtém um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccab1-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="ccab1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccab1-109">EXAMPLES</span></span>

### <span data-ttu-id="ccab1-110">1: recuperar um grupo de segurança de rede existente</span><span class="sxs-lookup"><span data-stu-id="ccab1-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="ccab1-111">Esse comando retorna o conteúdo do grupo de segurança de rede do Azure "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="ccab1-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="ccab1-112">OS</span><span class="sxs-lookup"><span data-stu-id="ccab1-112">PARAMETERS</span></span>

### <span data-ttu-id="ccab1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccab1-113">-DefaultProfile</span></span>
<span data-ttu-id="ccab1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccab1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccab1-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ccab1-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccab1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccab1-116">-Name</span></span>
<span data-ttu-id="ccab1-117">Especifica o nome do grupo de segurança de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ccab1-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccab1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccab1-118">-ResourceGroupName</span></span>
<span data-ttu-id="ccab1-119">Especifica o nome do grupo de recursos ao qual o grupo de segurança de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="ccab1-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccab1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccab1-120">CommonParameters</span></span>
<span data-ttu-id="ccab1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccab1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccab1-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccab1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccab1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccab1-123">INPUTS</span></span>

## <span data-ttu-id="ccab1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccab1-124">OUTPUTS</span></span>

### <span data-ttu-id="ccab1-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ccab1-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ccab1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccab1-126">NOTES</span></span>

## <span data-ttu-id="ccab1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccab1-127">RELATED LINKS</span></span>

[<span data-ttu-id="ccab1-128">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ccab1-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ccab1-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ccab1-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ccab1-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ccab1-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


