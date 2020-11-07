---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786291"
---
# <span data-ttu-id="23486-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="23486-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="23486-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23486-102">SYNOPSIS</span></span>
<span data-ttu-id="23486-103">Cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23486-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23486-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23486-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23486-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23486-105">DESCRIPTION</span></span>
<span data-ttu-id="23486-106">O cmdlet **New-AzureRmRouteTable** cria uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="23486-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="23486-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23486-107">EXAMPLES</span></span>

### <span data-ttu-id="23486-108">Exemplo 1: criar uma tabela de rota que contenha uma rota</span><span class="sxs-lookup"><span data-stu-id="23486-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="23486-109">O primeiro comando cria uma rota chamada Route07 usando o cmdlet New-AzureRmRouteConfig e a armazena na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="23486-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="23486-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="23486-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="23486-111">O segundo comando cria uma tabela de rota chamada RouteTable01 e adiciona a rota armazenada no $Route para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="23486-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="23486-112">O comando especifica o grupo de recursos ao qual a tabela pertence e o local da tabela.</span><span class="sxs-lookup"><span data-stu-id="23486-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="23486-113">OS</span><span class="sxs-lookup"><span data-stu-id="23486-113">PARAMETERS</span></span>

### <span data-ttu-id="23486-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23486-114">-AsJob</span></span>
<span data-ttu-id="23486-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23486-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23486-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23486-116">-DefaultProfile</span></span>
<span data-ttu-id="23486-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23486-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23486-118">-Force</span><span class="sxs-lookup"><span data-stu-id="23486-118">-Force</span></span>
<span data-ttu-id="23486-119">Indica que esse cmdlet cria uma tabela de rota mesmo que uma tabela de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="23486-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23486-120">-Local</span><span class="sxs-lookup"><span data-stu-id="23486-120">-Location</span></span>
<span data-ttu-id="23486-121">Especifica a região do Azure na qual esse cmdlet cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23486-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="23486-122">Para obter mais informações, consulte [regiões do Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="23486-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="23486-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="23486-123">-Name</span></span>
<span data-ttu-id="23486-124">Especifica um nome para a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23486-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23486-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23486-125">-ResourceGroupName</span></span>
<span data-ttu-id="23486-126">Especifica o nome do grupo de recursos em que esse cmdlet cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23486-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="23486-127">-Rota</span><span class="sxs-lookup"><span data-stu-id="23486-127">-Route</span></span>
<span data-ttu-id="23486-128">Especifica uma matriz de objetos de **rota** a serem associados à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23486-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23486-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="23486-129">-Tag</span></span>
<span data-ttu-id="23486-130">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="23486-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="23486-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="23486-131">For example:</span></span>

<span data-ttu-id="23486-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="23486-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23486-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23486-133">-Confirm</span></span>
<span data-ttu-id="23486-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23486-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23486-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23486-135">-WhatIf</span></span>
<span data-ttu-id="23486-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23486-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23486-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23486-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23486-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23486-138">CommonParameters</span></span>
<span data-ttu-id="23486-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23486-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23486-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23486-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23486-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23486-141">INPUTS</span></span>

## <span data-ttu-id="23486-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23486-142">OUTPUTS</span></span>

### <span data-ttu-id="23486-143">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="23486-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="23486-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23486-144">NOTES</span></span>

## <span data-ttu-id="23486-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23486-145">RELATED LINKS</span></span>

[<span data-ttu-id="23486-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="23486-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="23486-147">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="23486-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="23486-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="23486-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="23486-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="23486-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
