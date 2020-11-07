---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3aea2414a4b7fdfbc14e65d4d087bb7e31206aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773098"
---
# <span data-ttu-id="53444-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="53444-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="53444-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53444-102">SYNOPSIS</span></span>
<span data-ttu-id="53444-103">Obtém um link de rede virtual associado à zona DNS privada especificada.</span><span class="sxs-lookup"><span data-stu-id="53444-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="53444-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53444-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53444-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53444-105">DESCRIPTION</span></span>
<span data-ttu-id="53444-106">O cmdlet **Get-AzPrivateDnsVirtualNetworkLink** Obtém links de rede virtual associados a uma determinada zona de DNS particular do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="53444-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="53444-107">Se você especificar o parâmetro *Name* , um único objeto **PSPrivateDnsVirtualNetworkLink** será retornado.</span><span class="sxs-lookup"><span data-stu-id="53444-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="53444-108">Se você não especificar o parâmetro *Name* , uma matriz que contenha todos os links associados à zona no grupo de recursos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="53444-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="53444-109">Você pode usar o objeto **PSPrivateDnsVirtualNetworkLink** para atualizar o link.</span><span class="sxs-lookup"><span data-stu-id="53444-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="53444-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53444-110">EXAMPLES</span></span>

### <span data-ttu-id="53444-111">Exemplo 1: obter um link de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="53444-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="53444-112">Este exemplo obtém o link de rede virtual MyLink associado à zona DNS privada chamada myzone.com do grupo de recursos especificado e, em seguida, armazena-o na variável $Link.</span><span class="sxs-lookup"><span data-stu-id="53444-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="53444-113">Exemplo 2: obter todos os links associados a uma zona em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53444-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="53444-114">Este exemplo obtém todos os links de rede virtual associados à zona DNS privada "myzone.com" no grupo de recursos especificado e, em seguida, armazena-os na variável $Links.</span><span class="sxs-lookup"><span data-stu-id="53444-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="53444-115">OS</span><span class="sxs-lookup"><span data-stu-id="53444-115">PARAMETERS</span></span>

### <span data-ttu-id="53444-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53444-116">-DefaultProfile</span></span>
<span data-ttu-id="53444-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="53444-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53444-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="53444-118">-Name</span></span>
<span data-ttu-id="53444-119">Especifica o nome do link de rede virtual a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="53444-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="53444-120">Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todos os links associados à zona DNS privada especificada no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="53444-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53444-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53444-121">-ResourceGroupName</span></span>
<span data-ttu-id="53444-122">Especifica o nome do grupo de recursos que contém o link de rede virtual a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="53444-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53444-123">-Zonename</span><span class="sxs-lookup"><span data-stu-id="53444-123">-ZoneName</span></span>
<span data-ttu-id="53444-124">Especifica o nome da zona DNS privada à qual o link de rede virtual está vinculado.</span><span class="sxs-lookup"><span data-stu-id="53444-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53444-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53444-125">CommonParameters</span></span>
<span data-ttu-id="53444-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53444-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53444-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53444-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53444-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53444-128">INPUTS</span></span>

### <span data-ttu-id="53444-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53444-129">None</span></span>

## <span data-ttu-id="53444-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53444-130">OUTPUTS</span></span>

### <span data-ttu-id="53444-131">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="53444-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="53444-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53444-132">NOTES</span></span>

## <span data-ttu-id="53444-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53444-133">RELATED LINKS</span></span>

[<span data-ttu-id="53444-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="53444-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="53444-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="53444-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="53444-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="53444-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)