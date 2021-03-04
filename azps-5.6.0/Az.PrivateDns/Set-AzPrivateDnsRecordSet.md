---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889763"
---
# <span data-ttu-id="3d124-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3d124-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="3d124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d124-102">SYNOPSIS</span></span>
<span data-ttu-id="3d124-103">Atualizações/define um conjunto de registros em uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="3d124-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="3d124-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d124-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d124-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d124-105">DESCRIPTION</span></span>
<span data-ttu-id="3d124-106">O Set-AzPrivateDnsRecordSet atualiza um conjunto de registros no serviço DNS privado do Azure a partir de um objeto RecordSet local.</span><span class="sxs-lookup"><span data-stu-id="3d124-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="3d124-107">Você pode passar um objeto RecordSet como parâmetro ou usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d124-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="3d124-108">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3d124-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="3d124-109">O conjunto de registros não será atualizado se tiver sido alterado no DNS privado do Azure desde que o objeto RecordSet local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="3d124-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="3d124-110">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3d124-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="3d124-111">Você pode suprimir esse comportamento usando o parâmetro Overwrite, que atualiza o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3d124-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="3d124-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d124-112">EXAMPLES</span></span>

### <span data-ttu-id="3d124-113">Exemplo 1: Atualizar um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3d124-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="3d124-114">O primeiro comando usa o cmdlet Get-AzPrivateDnsRecordSet para obter o conjunto de registros especificado e o armazena na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3d124-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="3d124-115">O segundo e o terceiro comandos são operações off-line para adicionar dois registros A ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="3d124-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="3d124-116">O comando final usa o cmdlet Set-AzPrivateDnsRecordSet para confirmação da atualização.</span><span class="sxs-lookup"><span data-stu-id="3d124-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="3d124-117">Exemplo 2: atualizar um registro SOA</span><span class="sxs-lookup"><span data-stu-id="3d124-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="3d124-118">O primeiro comando usa o cmdlet Get-AzPrivateDnsRecordSet para obter o conjunto de registros especificado e o armazena na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3d124-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="3d124-119">O segundo comando atualiza o registro SOA especificado $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3d124-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="3d124-120">O comando final usa o cmdlet Set-AzPrivateDnsRecordSet para propagar a atualização em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3d124-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="3d124-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d124-121">PARAMETERS</span></span>

### <span data-ttu-id="3d124-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d124-122">-DefaultProfile</span></span>
<span data-ttu-id="3d124-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d124-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d124-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3d124-124">-Overwrite</span></span>
<span data-ttu-id="3d124-125">Não use o campo ETag do parâmetro RecordSet para verificações otimistas de simulta.</span><span class="sxs-lookup"><span data-stu-id="3d124-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="3d124-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="3d124-126">-RecordSet</span></span>
<span data-ttu-id="3d124-127">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="3d124-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="3d124-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d124-128">-Confirm</span></span>
<span data-ttu-id="3d124-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d124-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d124-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d124-130">-WhatIf</span></span>
<span data-ttu-id="3d124-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d124-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d124-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d124-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d124-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d124-133">CommonParameters</span></span>
<span data-ttu-id="3d124-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d124-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d124-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d124-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d124-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d124-136">INPUTS</span></span>

### <span data-ttu-id="3d124-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3d124-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="3d124-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d124-138">OUTPUTS</span></span>

### <span data-ttu-id="3d124-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3d124-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="3d124-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d124-140">NOTES</span></span>

## <span data-ttu-id="3d124-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d124-141">RELATED LINKS</span></span>
