---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776721"
---
# <span data-ttu-id="97996-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="97996-101">New-AzDnsZone</span></span>

## <span data-ttu-id="97996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97996-102">SYNOPSIS</span></span>
<span data-ttu-id="97996-103">Cria uma nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="97996-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="97996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97996-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97996-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97996-105">DESCRIPTION</span></span>
<span data-ttu-id="97996-106">O cmdlet **New-AzDnsZone** cria uma nova zona de sistema de nomes de domínio (DNS) no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="97996-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="97996-107">Você deve especificar um nome de zona DNS exclusivo para o parâmetro *Name* , ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="97996-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="97996-108">Após a criação da zona, use o cmdlet New-AzDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="97996-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="97996-109">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="97996-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="97996-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97996-110">EXAMPLES</span></span>

### <span data-ttu-id="97996-111">Exemplo 1: criar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="97996-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="97996-112">Esse comando cria uma nova zona DNS chamada myzone.com no grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="97996-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="97996-113">OS</span><span class="sxs-lookup"><span data-stu-id="97996-113">PARAMETERS</span></span>

### <span data-ttu-id="97996-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="97996-114">-Name</span></span>
<span data-ttu-id="97996-115">Especifica o nome da zona DNS a ser criada.</span><span class="sxs-lookup"><span data-stu-id="97996-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="97996-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97996-116">-ResourceGroupName</span></span>
<span data-ttu-id="97996-117">Especifica o grupo de recursos no qual a zona será criada.</span><span class="sxs-lookup"><span data-stu-id="97996-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="97996-118">-Marca</span><span class="sxs-lookup"><span data-stu-id="97996-118">-Tag</span></span>
<span data-ttu-id="97996-119">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="97996-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97996-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="97996-120">For example:</span></span>

<span data-ttu-id="97996-121">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="97996-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97996-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97996-122">-Confirm</span></span>
<span data-ttu-id="97996-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97996-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97996-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97996-124">-WhatIf</span></span>
<span data-ttu-id="97996-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97996-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97996-126">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97996-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97996-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97996-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97996-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97996-128">CommonParameters</span></span>
<span data-ttu-id="97996-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97996-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97996-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97996-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97996-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97996-131">INPUTS</span></span>

### <span data-ttu-id="97996-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97996-132">None</span></span>

<span data-ttu-id="97996-133">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97996-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="97996-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97996-134">OUTPUTS</span></span>

### <span data-ttu-id="97996-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="97996-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="97996-136">Esse cmdlet retorna um objeto Microsoft. Azure. Commands. DNS. DnsZone que representa a nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="97996-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="97996-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97996-137">NOTES</span></span>
<span data-ttu-id="97996-138">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="97996-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="97996-139">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="97996-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="97996-140">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="97996-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="97996-141">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="97996-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="97996-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97996-142">RELATED LINKS</span></span>

[<span data-ttu-id="97996-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="97996-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="97996-144">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="97996-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="97996-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="97996-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)