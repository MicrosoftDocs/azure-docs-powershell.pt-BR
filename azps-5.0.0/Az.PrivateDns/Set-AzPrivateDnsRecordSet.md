---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284191"
---
# <span data-ttu-id="caabc-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="caabc-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="caabc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="caabc-102">SYNOPSIS</span></span>
<span data-ttu-id="caabc-103">Atualiza/define um conjunto de registros em uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="caabc-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="caabc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caabc-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caabc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="caabc-105">DESCRIPTION</span></span>
<span data-ttu-id="caabc-106">O cmdlet Set-AzPrivateDnsRecordSet atualiza um conjunto de registros no serviço DNS privado do Azure de um objeto RecordSet local.</span><span class="sxs-lookup"><span data-stu-id="caabc-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="caabc-107">Você pode passar um objeto RecordSet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="caabc-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="caabc-108">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="caabc-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="caabc-109">O conjunto de registros não será atualizado se tiver sido alterado no DNS privado do Azure desde a recuperação do objeto RecordSet local.</span><span class="sxs-lookup"><span data-stu-id="caabc-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="caabc-110">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="caabc-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="caabc-111">Você pode suprimir esse comportamento usando o parâmetro overwrite, que atualiza o conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="caabc-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="caabc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caabc-112">EXAMPLES</span></span>

### <span data-ttu-id="caabc-113">Exemplo 1: atualizar um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="caabc-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="caabc-114">O primeiro comando usa o cmdlet Get-AzPrivateDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="caabc-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="caabc-115">O segundo e o terceiro comandos são operações off-line para adicionar dois registros a ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="caabc-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="caabc-116">O comando final usa o cmdlet Set-AzPrivateDnsRecordSet para confirmar a atualização.</span><span class="sxs-lookup"><span data-stu-id="caabc-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="caabc-117">Exemplo 2: atualizar um registro SOA</span><span class="sxs-lookup"><span data-stu-id="caabc-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="caabc-118">O primeiro comando usa o cmdlet Get-AzPrivateDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="caabc-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="caabc-119">O segundo comando atualiza o registro SOA especificado em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="caabc-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="caabc-120">O comando final usa o cmdlet Set-AzPrivateDnsRecordSet para propagar a atualização em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="caabc-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="caabc-121">OS</span><span class="sxs-lookup"><span data-stu-id="caabc-121">PARAMETERS</span></span>

### <span data-ttu-id="caabc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caabc-122">-DefaultProfile</span></span>
<span data-ttu-id="caabc-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="caabc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caabc-124">-Substituir</span><span class="sxs-lookup"><span data-stu-id="caabc-124">-Overwrite</span></span>
<span data-ttu-id="caabc-125">Não use o campo ETag do parâmetro RecordSet para verificações de simultaneidade otimistas.</span><span class="sxs-lookup"><span data-stu-id="caabc-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caabc-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="caabc-126">-RecordSet</span></span>
<span data-ttu-id="caabc-127">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="caabc-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caabc-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="caabc-128">-Confirm</span></span>
<span data-ttu-id="caabc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caabc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caabc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caabc-130">-WhatIf</span></span>
<span data-ttu-id="caabc-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="caabc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caabc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="caabc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caabc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caabc-133">CommonParameters</span></span>
<span data-ttu-id="caabc-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caabc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caabc-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caabc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caabc-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="caabc-136">INPUTS</span></span>

### <span data-ttu-id="caabc-137">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="caabc-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="caabc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="caabc-138">OUTPUTS</span></span>

### <span data-ttu-id="caabc-139">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="caabc-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="caabc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="caabc-140">NOTES</span></span>

## <span data-ttu-id="caabc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caabc-141">RELATED LINKS</span></span>
