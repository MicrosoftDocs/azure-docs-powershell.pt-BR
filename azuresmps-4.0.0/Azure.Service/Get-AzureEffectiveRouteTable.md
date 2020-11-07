---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946353"
---
# <span data-ttu-id="65c89-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="65c89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65c89-102">SYNOPSIS</span></span>
<span data-ttu-id="65c89-103">Obtém a rota aplicada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65c89-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="65c89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65c89-104">SYNTAX</span></span>

### <span data-ttu-id="65c89-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="65c89-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65c89-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="65c89-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65c89-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65c89-107">DESCRIPTION</span></span>
<span data-ttu-id="65c89-108">O cmdlet **Get-AzureEffectiveRouteTable** Obtém a rota aplicada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65c89-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="65c89-109">Esta operação pode demorar vários segundos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="65c89-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="65c89-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65c89-110">EXAMPLES</span></span>

### <span data-ttu-id="65c89-111">Exemplo 1: obter a rota efetiva aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="65c89-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="65c89-112">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="65c89-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="65c89-113">O cmdlet atual Obtém a rota aplicada a essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65c89-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="65c89-114">OS</span><span class="sxs-lookup"><span data-stu-id="65c89-114">PARAMETERS</span></span>

### <span data-ttu-id="65c89-115">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="65c89-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="65c89-116">Especifica o nome do adaptador de rede para o qual este cmdlet obtém rotas efetivas.</span><span class="sxs-lookup"><span data-stu-id="65c89-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="65c89-117">-Profile</span></span>
<span data-ttu-id="65c89-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="65c89-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="65c89-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="65c89-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="65c89-120">-RoleInstanceName</span></span>
<span data-ttu-id="65c89-121">Especifica o nome de uma função de PaaS para a qual esse cmdlet obtém rotas efetivas.</span><span class="sxs-lookup"><span data-stu-id="65c89-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="65c89-122">-ServiceName</span></span>
<span data-ttu-id="65c89-123">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="65c89-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="65c89-124">A função de PaaS para a qual este cmdlet obtém rotas efetivas pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="65c89-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="65c89-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="65c89-125">-Slot</span></span>
<span data-ttu-id="65c89-126">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="65c89-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="65c89-127">A função de PaaS para a qual este cmdlet obtém rotas efetivas tem o slot especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="65c89-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="65c89-128">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="65c89-128">Valid values are:</span></span> 

- <span data-ttu-id="65c89-129">Preparo</span><span class="sxs-lookup"><span data-stu-id="65c89-129">Production</span></span>
- <span data-ttu-id="65c89-130">Preparação</span><span class="sxs-lookup"><span data-stu-id="65c89-130">Staging</span></span> 

<span data-ttu-id="65c89-131">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="65c89-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-132">-VM</span><span class="sxs-lookup"><span data-stu-id="65c89-132">-VM</span></span>
<span data-ttu-id="65c89-133">Especifica o objeto da máquina virtual para o qual este cmdlet obtém rotas efetivas.</span><span class="sxs-lookup"><span data-stu-id="65c89-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c89-134">CommonParameters</span></span>
<span data-ttu-id="65c89-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c89-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c89-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c89-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65c89-137">INPUTS</span></span>

## <span data-ttu-id="65c89-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65c89-138">OUTPUTS</span></span>

### <span data-ttu-id="65c89-139">System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="65c89-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="65c89-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65c89-140">NOTES</span></span>

## <span data-ttu-id="65c89-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65c89-141">RELATED LINKS</span></span>

[<span data-ttu-id="65c89-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="65c89-143">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="65c89-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="65c89-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="65c89-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="65c89-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


