---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776732"
---
# <span data-ttu-id="51fe3-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="51fe3-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="51fe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="51fe3-103">Obtém uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="51fe3-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="51fe3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51fe3-104">SYNTAX</span></span>

### <span data-ttu-id="51fe3-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="51fe3-105">Default (Default)</span></span>
```
Get-AzDnsZone [<CommonParameters>]
```

### <span data-ttu-id="51fe3-106">Resource</span><span class="sxs-lookup"><span data-stu-id="51fe3-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="51fe3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51fe3-107">DESCRIPTION</span></span>
<span data-ttu-id="51fe3-108">O cmdlet **Get-AzDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="51fe3-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="51fe3-109">Se você especificar o parâmetro *Name* , um único objeto **dnsZone** será retornado.</span><span class="sxs-lookup"><span data-stu-id="51fe3-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="51fe3-110">Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="51fe3-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="51fe3-111">Você pode usar o objeto **dnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.</span><span class="sxs-lookup"><span data-stu-id="51fe3-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="51fe3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51fe3-112">EXAMPLES</span></span>

### <span data-ttu-id="51fe3-113">Exemplo 1: obter uma zona</span><span class="sxs-lookup"><span data-stu-id="51fe3-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="51fe3-114">Este exemplo obtém a zona DNS chamada myzone.com do grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="51fe3-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="51fe3-115">Exemplo 2: obter todas as zonas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="51fe3-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="51fe3-116">Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="51fe3-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="51fe3-117">Exemplo 3: obter todas as zonas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="51fe3-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="51fe3-118">Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="51fe3-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="51fe3-119">OS</span><span class="sxs-lookup"><span data-stu-id="51fe3-119">PARAMETERS</span></span>

### <span data-ttu-id="51fe3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="51fe3-120">-Name</span></span>
<span data-ttu-id="51fe3-121">Especifica o nome da zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="51fe3-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="51fe3-122">Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="51fe3-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="51fe3-123">Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="51fe3-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="51fe3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fe3-124">-ResourceGroupName</span></span>
<span data-ttu-id="51fe3-125">Especifica o nome do grupo de recursos que contém a zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="51fe3-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="51fe3-126">Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="51fe3-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="51fe3-127">Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="51fe3-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="51fe3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fe3-128">CommonParameters</span></span>
<span data-ttu-id="51fe3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51fe3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fe3-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fe3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fe3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51fe3-131">INPUTS</span></span>

### <span data-ttu-id="51fe3-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51fe3-132">None</span></span>
<span data-ttu-id="51fe3-133">Este cmdlet não permite que você entre na entrada de pipe.</span><span class="sxs-lookup"><span data-stu-id="51fe3-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="51fe3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51fe3-134">OUTPUTS</span></span>

### <span data-ttu-id="51fe3-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="51fe3-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="51fe3-136">Esse cmdlet retorna um objeto que representa a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="51fe3-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="51fe3-137">Se o nome da zona não for especificado, uma matriz de objetos de zona será retornada.</span><span class="sxs-lookup"><span data-stu-id="51fe3-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="51fe3-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51fe3-138">NOTES</span></span>

## <span data-ttu-id="51fe3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51fe3-139">RELATED LINKS</span></span>

[<span data-ttu-id="51fe3-140">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="51fe3-140">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="51fe3-141">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="51fe3-141">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="51fe3-142">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="51fe3-142">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
