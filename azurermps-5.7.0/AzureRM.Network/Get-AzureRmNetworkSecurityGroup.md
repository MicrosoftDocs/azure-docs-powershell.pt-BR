---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432465"
---
# <span data-ttu-id="6f3bb-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f3bb-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="6f3bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3bb-103">Obtém um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f3bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f3bb-104">SYNTAX</span></span>

### <span data-ttu-id="6f3bb-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="6f3bb-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f3bb-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="6f3bb-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f3bb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f3bb-107">DESCRIPTION</span></span>
<span data-ttu-id="6f3bb-108">O cmdlet **Get-AzureRmNetworkSecurityGroup** Obtém um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="6f3bb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f3bb-109">EXAMPLES</span></span>

### <span data-ttu-id="6f3bb-110">1: recuperar um grupo de segurança de rede existente</span><span class="sxs-lookup"><span data-stu-id="6f3bb-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="6f3bb-111">Esse comando retorna o conteúdo do grupo de segurança de rede do Azure "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="6f3bb-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="6f3bb-112">OS</span><span class="sxs-lookup"><span data-stu-id="6f3bb-112">PARAMETERS</span></span>

### <span data-ttu-id="6f3bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f3bb-113">-DefaultProfile</span></span>
<span data-ttu-id="6f3bb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f3bb-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6f3bb-115">-ExpandResource</span></span>
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

### <span data-ttu-id="6f3bb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f3bb-116">-Name</span></span>
<span data-ttu-id="6f3bb-117">Especifica o nome do grupo de segurança de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f3bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f3bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="6f3bb-119">Especifica o nome do grupo de recursos ao qual o grupo de segurança de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="6f3bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3bb-120">CommonParameters</span></span>
<span data-ttu-id="6f3bb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3bb-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f3bb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3bb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f3bb-123">INPUTS</span></span>

### <span data-ttu-id="6f3bb-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f3bb-124">None</span></span>
<span data-ttu-id="6f3bb-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6f3bb-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f3bb-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f3bb-126">OUTPUTS</span></span>

### <span data-ttu-id="6f3bb-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f3bb-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="6f3bb-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f3bb-128">NOTES</span></span>

## <span data-ttu-id="6f3bb-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f3bb-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f3bb-130">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f3bb-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="6f3bb-131">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f3bb-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="6f3bb-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f3bb-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


