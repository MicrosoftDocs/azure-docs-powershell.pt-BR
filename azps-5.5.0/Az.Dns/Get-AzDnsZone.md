---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117673"
---
# <span data-ttu-id="c439a-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c439a-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="c439a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c439a-102">SYNOPSIS</span></span>
<span data-ttu-id="c439a-103">Obtém uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="c439a-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="c439a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c439a-104">SYNTAX</span></span>

### <span data-ttu-id="c439a-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c439a-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c439a-106">Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c439a-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c439a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c439a-107">DESCRIPTION</span></span>
<span data-ttu-id="c439a-108">O cmdlet **Get-AzDnsZone** obtém uma zona DNS (Sistema de Nomes de Domínio) do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c439a-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="c439a-109">Se você especificar o *parâmetro Nome,* um único objeto **DnsZone** será retornado.</span><span class="sxs-lookup"><span data-stu-id="c439a-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="c439a-110">Se você não especificar o parâmetro *Nome,* uma matriz que contém todas as zonas no grupo de recursos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="c439a-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="c439a-111">Você pode usar o **objeto DnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **RecordSet** a ele.</span><span class="sxs-lookup"><span data-stu-id="c439a-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="c439a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c439a-112">EXAMPLES</span></span>

### <span data-ttu-id="c439a-113">Exemplo 1: Obter uma zona</span><span class="sxs-lookup"><span data-stu-id="c439a-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="c439a-114">Este exemplo obtém a zona DNS nomeada myzone.com do grupo de recursos especificado e a armazena na variável $Zone dados.</span><span class="sxs-lookup"><span data-stu-id="c439a-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="c439a-115">Exemplo 2: Obter todas as zonas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c439a-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c439a-116">Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones dados.</span><span class="sxs-lookup"><span data-stu-id="c439a-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="c439a-117">Exemplo 3: Obter todas as zonas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c439a-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="c439a-118">Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones usuário.</span><span class="sxs-lookup"><span data-stu-id="c439a-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="c439a-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c439a-119">PARAMETERS</span></span>

### <span data-ttu-id="c439a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c439a-120">-DefaultProfile</span></span>
<span data-ttu-id="c439a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c439a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c439a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c439a-122">-Name</span></span>
<span data-ttu-id="c439a-123">Especifica o nome da zona DNS a ser obter.</span><span class="sxs-lookup"><span data-stu-id="c439a-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="c439a-124">Se você não especificar um  valor para o parâmetro Nome, esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c439a-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="c439a-125">Se você também omitir o parâmetro *ResourceGroupName,* esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c439a-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="c439a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c439a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c439a-127">Especifica o nome do grupo de recursos que contém a zona DNS para obter.</span><span class="sxs-lookup"><span data-stu-id="c439a-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="c439a-128">Se você não especificar o *ResourceGroupName,* também deverá omitir o *parâmetro* Nome.</span><span class="sxs-lookup"><span data-stu-id="c439a-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="c439a-129">Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c439a-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="c439a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c439a-130">CommonParameters</span></span>
<span data-ttu-id="c439a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c439a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c439a-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c439a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c439a-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="c439a-133">INPUTS</span></span>

### <span data-ttu-id="c439a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c439a-134">System.String</span></span>

## <span data-ttu-id="c439a-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="c439a-135">OUTPUTS</span></span>

### <span data-ttu-id="c439a-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c439a-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c439a-137">Notas</span><span class="sxs-lookup"><span data-stu-id="c439a-137">NOTES</span></span>

## <span data-ttu-id="c439a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c439a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c439a-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c439a-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c439a-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c439a-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="c439a-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c439a-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
