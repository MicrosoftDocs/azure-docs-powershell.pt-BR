---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112915"
---
# <span data-ttu-id="92170-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="92170-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="92170-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92170-102">SYNOPSIS</span></span>
<span data-ttu-id="92170-103">Obtém uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="92170-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="92170-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92170-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92170-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92170-105">DESCRIPTION</span></span>
<span data-ttu-id="92170-106">O cmdlet **Get-AzPrivateDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) privada do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="92170-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="92170-107">Se você especificar o parâmetro *Name* , um único objeto **PrivateDnsZone** será retornado.</span><span class="sxs-lookup"><span data-stu-id="92170-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="92170-108">Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="92170-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="92170-109">Você pode usar o objeto **PrivateDnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.</span><span class="sxs-lookup"><span data-stu-id="92170-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="92170-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92170-110">EXAMPLES</span></span>

### <span data-ttu-id="92170-111">Exemplo 1: obter uma zona</span><span class="sxs-lookup"><span data-stu-id="92170-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="92170-112">Exemplo 2: obter todas as zonas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="92170-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="92170-113">Este exemplo obtém todas as zonas DNS privadas do grupo de recursos especificado e, em seguida, as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="92170-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="92170-114">Exemplo 3: obter todas as zonas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="92170-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="92170-115">Este exemplo obtém todas as zonas DNS particulares na assinatura atual do Azure e as armazena na variável $Zones.</span><span class="sxs-lookup"><span data-stu-id="92170-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="92170-116">OS</span><span class="sxs-lookup"><span data-stu-id="92170-116">PARAMETERS</span></span>

### <span data-ttu-id="92170-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92170-117">-DefaultProfile</span></span>
<span data-ttu-id="92170-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="92170-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92170-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="92170-119">-Name</span></span>
<span data-ttu-id="92170-120">Especifica o nome da zona DNS privada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="92170-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="92170-121">Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obterá todas as zonas DNS privadas no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="92170-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="92170-122">Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS privadas na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="92170-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="92170-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92170-123">-ResourceGroupName</span></span>
<span data-ttu-id="92170-124">Especifica o nome do grupo de recursos que contém a zona DNS privada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="92170-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="92170-125">Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="92170-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="92170-126">Nesse caso, esse cmdlet obtém todas as zonas DNS privadas na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="92170-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="92170-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92170-127">CommonParameters</span></span>
<span data-ttu-id="92170-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92170-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92170-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92170-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92170-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92170-130">INPUTS</span></span>

### <span data-ttu-id="92170-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="92170-131">None</span></span>

## <span data-ttu-id="92170-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92170-132">OUTPUTS</span></span>

### <span data-ttu-id="92170-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="92170-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="92170-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92170-134">NOTES</span></span>

## <span data-ttu-id="92170-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92170-135">RELATED LINKS</span></span>

[<span data-ttu-id="92170-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="92170-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="92170-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="92170-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="92170-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="92170-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
