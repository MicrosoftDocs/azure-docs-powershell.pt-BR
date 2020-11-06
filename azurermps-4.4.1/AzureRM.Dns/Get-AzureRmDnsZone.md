---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610007"
---
# <span data-ttu-id="67a57-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67a57-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="67a57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67a57-102">SYNOPSIS</span></span>
<span data-ttu-id="67a57-103">Obtém uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="67a57-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67a57-104">SYNTAX</span></span>

### <span data-ttu-id="67a57-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="67a57-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a57-106">Resource</span><span class="sxs-lookup"><span data-stu-id="67a57-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67a57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67a57-107">DESCRIPTION</span></span>
<span data-ttu-id="67a57-108">O cmdlet **Get-AzureRmDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="67a57-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="67a57-109">Se você especificar o parâmetro *Name* , um único objeto **dnsZone** será retornado.</span><span class="sxs-lookup"><span data-stu-id="67a57-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="67a57-110">Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="67a57-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="67a57-111">Você pode usar o objeto **dnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.</span><span class="sxs-lookup"><span data-stu-id="67a57-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="67a57-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67a57-112">EXAMPLES</span></span>

### <span data-ttu-id="67a57-113">Exemplo 1: obter uma zona</span><span class="sxs-lookup"><span data-stu-id="67a57-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="67a57-114">Este exemplo obtém a zona DNS chamada myzone.com do grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="67a57-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="67a57-115">Exemplo 2: obter todas as zonas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="67a57-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="67a57-116">Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="67a57-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="67a57-117">Exemplo 3: obter todas as zonas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="67a57-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="67a57-118">Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="67a57-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="67a57-119">OS</span><span class="sxs-lookup"><span data-stu-id="67a57-119">PARAMETERS</span></span>

### <span data-ttu-id="67a57-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="67a57-120">-Name</span></span>
<span data-ttu-id="67a57-121">Especifica o nome da zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="67a57-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="67a57-122">Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="67a57-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="67a57-123">Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="67a57-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a57-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a57-124">-ResourceGroupName</span></span>
<span data-ttu-id="67a57-125">Especifica o nome do grupo de recursos que contém a zona DNS a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="67a57-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="67a57-126">Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="67a57-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="67a57-127">Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="67a57-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a57-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a57-128">-DefaultProfile</span></span>
<span data-ttu-id="67a57-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67a57-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a57-130">CommonParameters</span></span>
<span data-ttu-id="67a57-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a57-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a57-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a57-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67a57-133">INPUTS</span></span>

### <span data-ttu-id="67a57-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="67a57-134">None</span></span>
<span data-ttu-id="67a57-135">Este cmdlet não permite que você entre na entrada de pipe.</span><span class="sxs-lookup"><span data-stu-id="67a57-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="67a57-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67a57-136">OUTPUTS</span></span>

### <span data-ttu-id="67a57-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="67a57-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="67a57-138">Esse cmdlet retorna um objeto que representa a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="67a57-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="67a57-139">Se o nome da zona não for especificado, uma matriz de objetos de zona será retornada.</span><span class="sxs-lookup"><span data-stu-id="67a57-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="67a57-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67a57-140">NOTES</span></span>

## <span data-ttu-id="67a57-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67a57-141">RELATED LINKS</span></span>

[<span data-ttu-id="67a57-142">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67a57-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="67a57-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67a57-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="67a57-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67a57-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
