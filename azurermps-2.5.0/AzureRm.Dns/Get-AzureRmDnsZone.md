---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786116"
---
# <span data-ttu-id="d051e-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d051e-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="d051e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d051e-102">SYNOPSIS</span></span>
<span data-ttu-id="d051e-103">Obtém uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="d051e-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d051e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d051e-104">SYNTAX</span></span>

### <span data-ttu-id="d051e-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="d051e-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="d051e-106">Resource</span><span class="sxs-lookup"><span data-stu-id="d051e-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="d051e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d051e-107">DESCRIPTION</span></span>
<span data-ttu-id="d051e-108">O cmdlet **Get-AzureRmDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d051e-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="d051e-109">Se você especificar o parâmetro *Name* , um único objeto **dnsZone** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d051e-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="d051e-110">Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d051e-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="d051e-111">Você pode usar o objeto **dnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.</span><span class="sxs-lookup"><span data-stu-id="d051e-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="d051e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d051e-112">EXAMPLES</span></span>

### <span data-ttu-id="d051e-113">Exemplo 1: obter uma zona</span><span class="sxs-lookup"><span data-stu-id="d051e-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="d051e-114">Este exemplo obtém a zona DNS chamada myzone.com do grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="d051e-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d051e-115">Exemplo 2: obter todas as zonas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d051e-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d051e-116">Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="d051e-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="d051e-117">Exemplo 3: obter todas as zonas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d051e-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="d051e-118">Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="d051e-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="d051e-119">OS</span><span class="sxs-lookup"><span data-stu-id="d051e-119">PARAMETERS</span></span>

### <span data-ttu-id="d051e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d051e-120">-Name</span></span>
<span data-ttu-id="d051e-121">Especifica o nome da zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="d051e-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="d051e-122">Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d051e-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="d051e-123">Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d051e-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d051e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d051e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d051e-125">Especifica o nome do grupo de recursos que contém a zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="d051e-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="d051e-126">Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="d051e-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="d051e-127">Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d051e-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d051e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d051e-128">CommonParameters</span></span>
<span data-ttu-id="d051e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d051e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d051e-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d051e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d051e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d051e-131">INPUTS</span></span>

### <span data-ttu-id="d051e-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d051e-132">None</span></span>
<span data-ttu-id="d051e-133">Este cmdlet não permite que você entre na entrada de pipe.</span><span class="sxs-lookup"><span data-stu-id="d051e-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="d051e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d051e-134">OUTPUTS</span></span>

### <span data-ttu-id="d051e-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="d051e-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d051e-136">Esse cmdlet retorna um objeto que representa a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="d051e-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="d051e-137">Se o nome da zona não for especificado, uma matriz de objetos de zona será retornada.</span><span class="sxs-lookup"><span data-stu-id="d051e-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="d051e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d051e-138">NOTES</span></span>

## <span data-ttu-id="d051e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d051e-139">RELATED LINKS</span></span>

[<span data-ttu-id="d051e-140">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d051e-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="d051e-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d051e-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="d051e-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d051e-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
